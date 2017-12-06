---
title: "编写数据库提供程序的 EF 核心"
author: anmiller
ms.author: divega
ms.date: 10/27/2016
ms.assetid: 1165e2ec-e421-43fc-92ab-d92f9ab3c494
ms.technology: entity-framework-core
uid: core/providers/writing-a-provider
ms.openlocfilehash: 9d6d3748a9097b3b8eeee2a8a516c53f3b2afa58
ms.sourcegitcommit: 01a75cd483c1943ddd6f82af971f07abde20912e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2017
---
# <a name="writing-a-database-provider"></a><span data-ttu-id="4497c-102">编写数据库提供程序</span><span class="sxs-lookup"><span data-stu-id="4497c-102">Writing a Database Provider</span></span>

<span data-ttu-id="4497c-103">有关编写实体框架核心数据库提供程序的信息，请参阅[因此你想要编写 EF 核心提供程序](https://blog.oneunicorn.com/2016/11/11/so-you-want-to-write-an-ef-core-provider/)通过[Arthur Vickers](https://github.com/ajcvickers)。</span><span class="sxs-lookup"><span data-stu-id="4497c-103">For information about writing an Entity Framework Core database provider, see [So you want to write an EF Core provider](https://blog.oneunicorn.com/2016/11/11/so-you-want-to-write-an-ef-core-provider/) by [Arthur Vickers](https://github.com/ajcvickers).</span></span>

<span data-ttu-id="4497c-104">基本 EF 核心代码属于开放源代码，包含多个数据库提供程序可以使用作为参考。</span><span class="sxs-lookup"><span data-stu-id="4497c-104">The EF Core code base is open source and contains several database providers that can be used as a reference.</span></span> <span data-ttu-id="4497c-105">你可以在 https://github.com/aspnet/EntityFramework 找到源代码。</span><span class="sxs-lookup"><span data-stu-id="4497c-105">You can find the source code at https://github.com/aspnet/EntityFramework.</span></span>

## <a name="the-providers-beware-label"></a><span data-ttu-id="4497c-106">提供程序注意标签</span><span class="sxs-lookup"><span data-stu-id="4497c-106">The providers-beware label</span></span>

<span data-ttu-id="4497c-107">一旦开始于提供程序的工作，监视[ `providers-beware` ](https://github.com/aspnet/EntityFramework/labels/providers-beware)在我们的 GitHub 问题和拉取请求的标签。</span><span class="sxs-lookup"><span data-stu-id="4497c-107">Once you begin work on a provider, watch for the [`providers-beware`](https://github.com/aspnet/EntityFramework/labels/providers-beware) label on our GitHub issues and pull requests.</span></span> <span data-ttu-id="4497c-108">我们使用此标签来标识可能会影响提供程序编写器的更改。</span><span class="sxs-lookup"><span data-stu-id="4497c-108">We use this label to identify changes that may impact provider writers.</span></span>

## <a name="suggested-naming-of-third-party-providers"></a><span data-ttu-id="4497c-109">建议的第三方提供程序命名</span><span class="sxs-lookup"><span data-stu-id="4497c-109">Suggested naming of third party providers</span></span>

<span data-ttu-id="4497c-110">我们建议使用 NuGet 包的以下命名。</span><span class="sxs-lookup"><span data-stu-id="4497c-110">We suggest using the following naming for NuGet packages.</span></span> <span data-ttu-id="4497c-111">这是与 EF 核心小组所传递的包名称一致。</span><span class="sxs-lookup"><span data-stu-id="4497c-111">This is consistent with the names of packages delivered by the EF Core team.</span></span>

`<Optional project/company name>.EntityFrameworkCore.<Database engine name>`

<span data-ttu-id="4497c-112">例如：</span><span class="sxs-lookup"><span data-stu-id="4497c-112">For example:</span></span>
* `Microsoft.EntityFrameworkCore.SqlServer`
* `Npgsql.EntityFrameworkCore.PostgreSQL`
* `EntityFrameworkCore.SqlServerCompact40`