---
title: 数据库优先的 EF6
author: divega
ms.date: 2016-10-23
ms.assetid: cc6ffdb3-388d-4e79-a201-01ec2577c949
ms.openlocfilehash: 93ae5729e487ed9be3972ac78d599dbea19ed458
ms.sourcegitcommit: 0d36e8ff0892b7f034b765b15e041f375f88579a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2018
ms.locfileid: "44251084"
---
# <a name="database-first"></a><span data-ttu-id="2bce5-102">数据库优先</span><span class="sxs-lookup"><span data-stu-id="2bce5-102">Database First</span></span>
<span data-ttu-id="2bce5-103">此视频和分步演练会提供使用 Entity Framework 数据库优先开发的简介。</span><span class="sxs-lookup"><span data-stu-id="2bce5-103">This video and step-by-step walkthrough provide an introduction to Database First development using Entity Framework.</span></span> <span data-ttu-id="2bce5-104">数据库第一次可以进行反向工程，从现有数据库的模型。</span><span class="sxs-lookup"><span data-stu-id="2bce5-104">Database First allows you to reverse engineer a model from an existing database.</span></span> <span data-ttu-id="2bce5-105">模型存储在 EDMX 文件 （扩展名为.edmx） 并可以查看和编辑实体框架设计器中。</span><span class="sxs-lookup"><span data-stu-id="2bce5-105">The model is stored in an EDMX file (.edmx extension) and can be viewed and edited in the Entity Framework Designer.</span></span> <span data-ttu-id="2bce5-106">从 EDMX 文件自动生成与交互应用程序中的类。</span><span class="sxs-lookup"><span data-stu-id="2bce5-106">The classes that you interact with in your application are automatically generated from the EDMX file.</span></span>

## <a name="watch-the-video"></a><span data-ttu-id="2bce5-107">观看视频</span><span class="sxs-lookup"><span data-stu-id="2bce5-107">Watch the video</span></span>
<span data-ttu-id="2bce5-108">此视频提供了使用 Entity Framework 数据库优先开发的简介。</span><span class="sxs-lookup"><span data-stu-id="2bce5-108">This video provides an introduction to Database First development using Entity Framework.</span></span> <span data-ttu-id="2bce5-109">数据库第一次可以进行反向工程，从现有数据库的模型。</span><span class="sxs-lookup"><span data-stu-id="2bce5-109">Database First allows you to reverse engineer a model from an existing database.</span></span> <span data-ttu-id="2bce5-110">模型存储在 EDMX 文件 （扩展名为.edmx） 并可以查看和编辑实体框架设计器中。</span><span class="sxs-lookup"><span data-stu-id="2bce5-110">The model is stored in an EDMX file (.edmx extension) and can be viewed and edited in the Entity Framework Designer.</span></span> <span data-ttu-id="2bce5-111">从 EDMX 文件自动生成与交互应用程序中的类。</span><span class="sxs-lookup"><span data-stu-id="2bce5-111">The classes that you interact with in your application are automatically generated from the EDMX file.</span></span>

<span data-ttu-id="2bce5-112">**主讲人**：[Rowan Miller](http://romiller.com/)</span><span class="sxs-lookup"><span data-stu-id="2bce5-112">**Presented By**: [Rowan Miller](http://romiller.com/)</span></span>

<span data-ttu-id="2bce5-113">**视频**: [WMV](http://download.microsoft.com/download/8/F/0/8F0B5F63-4939-4DC8-A726-FF139B37F8D8/HDI-ITPro-MSDN-winvideo-databasefirst.wmv) | [MP4](http://download.microsoft.com/download/8/F/0/8F0B5F63-4939-4DC8-A726-FF139B37F8D8/HDI-ITPro-MSDN-mp4video-databasefirst.m4v) | [WMV (ZIP)](http://download.microsoft.com/download/8/F/0/8F0B5F63-4939-4DC8-A726-FF139B37F8D8/HDI-ITPro-MSDN-winvideo-databasefirst.zip)</span><span class="sxs-lookup"><span data-stu-id="2bce5-113">**Video**: [WMV](http://download.microsoft.com/download/8/F/0/8F0B5F63-4939-4DC8-A726-FF139B37F8D8/HDI-ITPro-MSDN-winvideo-databasefirst.wmv) | [MP4](http://download.microsoft.com/download/8/F/0/8F0B5F63-4939-4DC8-A726-FF139B37F8D8/HDI-ITPro-MSDN-mp4video-databasefirst.m4v) | [WMV (ZIP)](http://download.microsoft.com/download/8/F/0/8F0B5F63-4939-4DC8-A726-FF139B37F8D8/HDI-ITPro-MSDN-winvideo-databasefirst.zip)</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="2bce5-114">系统必备组件</span><span class="sxs-lookup"><span data-stu-id="2bce5-114">Pre-Requisites</span></span>

<span data-ttu-id="2bce5-115">将需要安装最低版本为 Visual Studio 2010 或 Visual Studio 2012 安装来完成本演练。</span><span class="sxs-lookup"><span data-stu-id="2bce5-115">You will need to have at least Visual Studio 2010 or Visual Studio 2012 installed to complete this walkthrough.</span></span>

<span data-ttu-id="2bce5-116">如果使用 Visual Studio 2010，您还需要具有[NuGet](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c)安装。</span><span class="sxs-lookup"><span data-stu-id="2bce5-116">If you are using Visual Studio 2010, you will also need to have [NuGet](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c) installed.</span></span>

 

## <a name="1-create-an-existing-database"></a><span data-ttu-id="2bce5-117">1.创建现有数据库</span><span class="sxs-lookup"><span data-stu-id="2bce5-117">1. Create an Existing Database</span></span>

<span data-ttu-id="2bce5-118">通常当你面向的现有数据库，则将已创建，但我们需要在本演练中创建的数据库访问。</span><span class="sxs-lookup"><span data-stu-id="2bce5-118">Typically when you are targeting an existing database it will already be created, but for this walkthrough we need to create a database to access.</span></span>

<span data-ttu-id="2bce5-119">随 Visual Studio 一起安装的数据库服务器是已安装的 Visual Studio 的版本而异：</span><span class="sxs-lookup"><span data-stu-id="2bce5-119">The database server that is installed with Visual Studio is different depending on the version of Visual Studio you have installed:</span></span>

-   <span data-ttu-id="2bce5-120">如果您使用的 Visual Studio 2010 系统将创建一个 SQL Express 数据库。</span><span class="sxs-lookup"><span data-stu-id="2bce5-120">If you are using Visual Studio 2010 you'll be creating a SQL Express database.</span></span>
-   <span data-ttu-id="2bce5-121">如果你正在使用 Visual Studio 2012，则您将创建[LocalDB](https://msdn.microsoft.com/library/hh510202(v=sql.110).aspx)数据库。</span><span class="sxs-lookup"><span data-stu-id="2bce5-121">If you are using Visual Studio 2012 then you'll be creating a [LocalDB](https://msdn.microsoft.com/library/hh510202(v=sql.110).aspx) database.</span></span>

 

<span data-ttu-id="2bce5-122">让我们继续并生成的数据库。</span><span class="sxs-lookup"><span data-stu-id="2bce5-122">Let's go ahead and generate the database.</span></span>

-   <span data-ttu-id="2bce5-123">打开 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2bce5-123">Open Visual Studio</span></span>
-   <span data-ttu-id="2bce5-124">**视图-&gt;服务器资源管理器**</span><span class="sxs-lookup"><span data-stu-id="2bce5-124">**View -&gt; Server Explorer**</span></span>
-   <span data-ttu-id="2bce5-125">右键单击**数据连接-&gt;添加连接...**</span><span class="sxs-lookup"><span data-stu-id="2bce5-125">Right click on **Data Connections -&gt; Add Connection…**</span></span>
-   <span data-ttu-id="2bce5-126">如果你尚未连接到数据库服务器资源管理器之前将需要选择 Microsoft SQL Server 作为数据源</span><span class="sxs-lookup"><span data-stu-id="2bce5-126">If you haven’t connected to a database from Server Explorer before you’ll need to select Microsoft SQL Server as the data source</span></span>

    ![选择数据源](~/ef6/media/selectdatasource.png)

-   <span data-ttu-id="2bce5-128">连接到 LocalDB 或 SQL Express，具体取决于哪一个已安装，并输入**DatabaseFirst.Blogging**作为数据库名称</span><span class="sxs-lookup"><span data-stu-id="2bce5-128">Connect to either LocalDB or SQL Express, depending on which one you have installed, and enter **DatabaseFirst.Blogging** as the database name</span></span>

    ![Sql Express 连接 DF](~/ef6/media/sqlexpressconnectiondf.png)

    ![LocalDB 连接 DF](~/ef6/media/localdbconnectiondf.png)

-   <span data-ttu-id="2bce5-131">选择**确定**并将你想要创建新数据库，请选择要求你**是**</span><span class="sxs-lookup"><span data-stu-id="2bce5-131">Select **OK** and you will be asked if you want to create a new database, select **Yes**</span></span>

    ![创建数据库对话框](~/ef6/media/createdatabasedialog.png)

-   <span data-ttu-id="2bce5-133">新数据库现在将出现在服务器资源管理器，右键单击它并选择**新查询**</span><span class="sxs-lookup"><span data-stu-id="2bce5-133">The new database will now appear in Server Explorer, right-click on it and select **New Query**</span></span>
-   <span data-ttu-id="2bce5-134">将下面的 SQL 复制到新的查询，然后右键单击查询并选择**Execute**</span><span class="sxs-lookup"><span data-stu-id="2bce5-134">Copy the following SQL into the new query, then right-click on the query and select **Execute**</span></span>

``` SQL
CREATE TABLE [dbo].[Blogs] (
    [BlogId] INT IDENTITY (1, 1) NOT NULL,
    [Name] NVARCHAR (200) NULL,
    [Url]  NVARCHAR (200) NULL,
    CONSTRAINT [PK_dbo.Blogs] PRIMARY KEY CLUSTERED ([BlogId] ASC)
);

CREATE TABLE [dbo].[Posts] (
    [PostId] INT IDENTITY (1, 1) NOT NULL,
    [Title] NVARCHAR (200) NULL,
    [Content] NTEXT NULL,
    [BlogId] INT NOT NULL,
    CONSTRAINT [PK_dbo.Posts] PRIMARY KEY CLUSTERED ([PostId] ASC),
    CONSTRAINT [FK_dbo.Posts_dbo.Blogs_BlogId] FOREIGN KEY ([BlogId]) REFERENCES [dbo].[Blogs] ([BlogId]) ON DELETE CASCADE
);
```

## <a name="2-create-the-application"></a><span data-ttu-id="2bce5-135">2.创建应用程序</span><span class="sxs-lookup"><span data-stu-id="2bce5-135">2. Create the Application</span></span>

<span data-ttu-id="2bce5-136">为了简单起见，我们要构建使用 Database First 来执行数据访问的基本的控制台应用程序：</span><span class="sxs-lookup"><span data-stu-id="2bce5-136">To keep things simple we’re going to build a basic console application that uses the Database First to perform data access:</span></span>

-   <span data-ttu-id="2bce5-137">打开 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2bce5-137">Open Visual Studio</span></span>
-   <span data-ttu-id="2bce5-138">**文件-&gt;新增-&gt;项目...**</span><span class="sxs-lookup"><span data-stu-id="2bce5-138">**File -&gt; New -&gt; Project…**</span></span>
-   <span data-ttu-id="2bce5-139">选择**Windows**左侧的菜单和**控制台应用程序**</span><span class="sxs-lookup"><span data-stu-id="2bce5-139">Select **Windows** from the left menu and **Console Application**</span></span>
-   <span data-ttu-id="2bce5-140">输入**DatabaseFirstSample**作为名称</span><span class="sxs-lookup"><span data-stu-id="2bce5-140">Enter **DatabaseFirstSample** as the name</span></span>
-   <span data-ttu-id="2bce5-141">选择“确定”</span><span class="sxs-lookup"><span data-stu-id="2bce5-141">Select **OK**</span></span>

 

## <a name="3-reverse-engineer-model"></a><span data-ttu-id="2bce5-142">3.反向工程模型</span><span class="sxs-lookup"><span data-stu-id="2bce5-142">3. Reverse Engineer Model</span></span>

<span data-ttu-id="2bce5-143">我们将使用实体框架设计器，它是作为 Visual Studio 的一部分，若要创建我们的模型。</span><span class="sxs-lookup"><span data-stu-id="2bce5-143">We’re going to make use of Entity Framework Designer, which is included as part of Visual Studio, to create our model.</span></span>

-   <span data-ttu-id="2bce5-144">**项目-&gt;添加新项...**</span><span class="sxs-lookup"><span data-stu-id="2bce5-144">**Project -&gt; Add New Item…**</span></span>
-   <span data-ttu-id="2bce5-145">选择**数据**左侧的菜单，然后**ADO.NET 实体数据模型**</span><span class="sxs-lookup"><span data-stu-id="2bce5-145">Select **Data** from the left menu and then **ADO.NET Entity Data Model**</span></span>
-   <span data-ttu-id="2bce5-146">输入**BloggingModel**作为名称，然后单击**确定**</span><span class="sxs-lookup"><span data-stu-id="2bce5-146">Enter **BloggingModel** as the name and click **OK**</span></span>
-   <span data-ttu-id="2bce5-147">这将启动**实体数据模型向导**</span><span class="sxs-lookup"><span data-stu-id="2bce5-147">This launches the **Entity Data Model Wizard**</span></span>
-   <span data-ttu-id="2bce5-148">选择**从数据库生成**单击**下一步**</span><span class="sxs-lookup"><span data-stu-id="2bce5-148">Select **Generate from Database** and click **Next**</span></span>

    ![向导步骤 1](~/ef6/media/wizardstep1.png)

-   <span data-ttu-id="2bce5-150">选择连接到第一个部分中创建的数据库中，输入**bloggingcontext**作为名称的连接字符串和单击**下一步**</span><span class="sxs-lookup"><span data-stu-id="2bce5-150">Select the connection to the database you created in the first section, enter **BloggingContext** as the name of the connection string and click **Next**</span></span>

    ![向导步骤 2](~/ef6/media/wizardstep2.png)

-   <span data-ttu-id="2bce5-152">单击表导入的所有表并单击完成旁边的复选框</span><span class="sxs-lookup"><span data-stu-id="2bce5-152">Click the checkbox next to ‘Tables’ to import all tables and click ‘Finish’</span></span>

    ![向导步骤 3](~/ef6/media/wizardstep3.png)

 

<span data-ttu-id="2bce5-154">反向工程过程完成后的新模型添加到你的项目，并打开，以便在实体框架设计器中查看。</span><span class="sxs-lookup"><span data-stu-id="2bce5-154">Once the reverse engineer process completes the new model is added to your project and opened up for you to view in the Entity Framework Designer.</span></span> <span data-ttu-id="2bce5-155">此外具有已 App.config 文件添加到你的项目数据库的连接详细信息。</span><span class="sxs-lookup"><span data-stu-id="2bce5-155">An App.config file has also been added to your project with the connection details for the database.</span></span>

![初始的模型](~/ef6/media/modelinitial.png)

### <a name="additional-steps-in-visual-studio-2010"></a><span data-ttu-id="2bce5-157">Visual Studio 2010 中的其他步骤</span><span class="sxs-lookup"><span data-stu-id="2bce5-157">Additional Steps in Visual Studio 2010</span></span>

<span data-ttu-id="2bce5-158">如果您正在一些其他步骤，您需要按照升级到 Entity Framework 的最新版本的 Visual Studio 2010 中。</span><span class="sxs-lookup"><span data-stu-id="2bce5-158">If you are working in Visual Studio 2010 there are some additional steps you need to follow to upgrade to the latest version of Entity Framework.</span></span> <span data-ttu-id="2bce5-159">升级非常重要，因为它可让你访问的改进了的 API 图面，为更易于使用，以及最新 bug 修补程序。</span><span class="sxs-lookup"><span data-stu-id="2bce5-159">Upgrading is important because it gives you access to an improved API surface, that is much easier to use, as well as the latest bug fixes.</span></span>

<span data-ttu-id="2bce5-160">首先，我们需要从 NuGet 获取实体框架的最新版本。</span><span class="sxs-lookup"><span data-stu-id="2bce5-160">First up, we need to get the latest version of Entity Framework from NuGet.</span></span>

-   <span data-ttu-id="2bce5-161">**项目 –&gt;管理 NuGet 包...** 
    *如果你没有\*\*管理 NuGet 包...*\* 选项应该安装[最新版本的 NuGet](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c)\*</span><span class="sxs-lookup"><span data-stu-id="2bce5-161">**Project –&gt; Manage NuGet Packages…**
*If you don’t have the **Manage NuGet Packages…** option you should install the [latest version of NuGet](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c)*</span></span>
-   <span data-ttu-id="2bce5-162">选择**Online**选项卡</span><span class="sxs-lookup"><span data-stu-id="2bce5-162">Select the **Online** tab</span></span>
-   <span data-ttu-id="2bce5-163">选择**EntityFramework**包</span><span class="sxs-lookup"><span data-stu-id="2bce5-163">Select the **EntityFramework** package</span></span>
-   <span data-ttu-id="2bce5-164">单击**安装**</span><span class="sxs-lookup"><span data-stu-id="2bce5-164">Click **Install**</span></span>

<span data-ttu-id="2bce5-165">接下来，我们需要交换我们的模型来生成利用了 DbContext API，在实体框架的更高版本中引入的代码。</span><span class="sxs-lookup"><span data-stu-id="2bce5-165">Next, we need to swap our model to generate code that makes use of the DbContext API, which was introduced in later versions of Entity Framework.</span></span>

-   <span data-ttu-id="2bce5-166">在您的模型在 EF 设计器中的某一空白点上右键单击并选择**添加代码生成项...**</span><span class="sxs-lookup"><span data-stu-id="2bce5-166">Right-click on an empty spot of your model in the EF Designer and select **Add Code Generation Item…**</span></span>
-   <span data-ttu-id="2bce5-167">选择**联机模板**从左侧的菜单并搜索**DbContext**</span><span class="sxs-lookup"><span data-stu-id="2bce5-167">Select **Online Templates** from the left menu and search for **DbContext**</span></span>
-   <span data-ttu-id="2bce5-168">选择 EF **5.x DbContext 生成器 C\#**，输入**BloggingModel**作为名称，然后单击**添加**</span><span class="sxs-lookup"><span data-stu-id="2bce5-168">Select the EF **5.x DbContext Generator for C\#**, enter **BloggingModel** as the name and click **Add**</span></span>

    ![DbContext 模板](~/ef6/media/dbcontexttemplate.png)

 

## <a name="4-reading--writing-data"></a><span data-ttu-id="2bce5-170">4.读取和写入数据</span><span class="sxs-lookup"><span data-stu-id="2bce5-170">4. Reading & Writing Data</span></span>

<span data-ttu-id="2bce5-171">现在，我们有一个模型就可以使用它来访问某些数据。</span><span class="sxs-lookup"><span data-stu-id="2bce5-171">Now that we have a model it’s time to use it to access some data.</span></span> <span data-ttu-id="2bce5-172">我们将这些类用于访问数据在自动生成的基于 EDMX 文件。</span><span class="sxs-lookup"><span data-stu-id="2bce5-172">The classes we are going to use to access data are being automatically generated for you based on the EDMX file.</span></span>

<span data-ttu-id="2bce5-173">*此屏幕截图取自 Visual Studio 2012 中，如果您使用的 Visual Studio 2010 BloggingModel.tt 并 BloggingModel.Context.tt 文件将直接位于你的项目而不是嵌套在 EDMX 文件下。*</span><span class="sxs-lookup"><span data-stu-id="2bce5-173">*This screen shot is from Visual Studio 2012, if you are using Visual Studio 2010 the BloggingModel.tt and BloggingModel.Context.tt files will be directly under your project rather than nested under the EDMX file.*</span></span>

![生成的类 DF](~/ef6/media/generatedclassesdf.png)

 

<span data-ttu-id="2bce5-175">在 Program.cs 中实现的 Main 方法，如下所示。</span><span class="sxs-lookup"><span data-stu-id="2bce5-175">Implement the Main method in Program.cs as shown below.</span></span> <span data-ttu-id="2bce5-176">此代码将创建我们的上下文的新实例，并使用它来插入新博客。</span><span class="sxs-lookup"><span data-stu-id="2bce5-176">This code creates a new instance of our context and then uses it to insert a new Blog.</span></span> <span data-ttu-id="2bce5-177">然后它使用 LINQ 查询以从按标题按字母顺序排序的数据库中检索所有博客。</span><span class="sxs-lookup"><span data-stu-id="2bce5-177">Then it uses a LINQ query to retrieve all Blogs from the database ordered alphabetically by Title.</span></span>

``` csharp
class Program
{
    static void Main(string[] args)
    {
        using (var db = new BloggingContext())
        {
            // Create and save a new Blog
            Console.Write("Enter a name for a new Blog: ");
            var name = Console.ReadLine();

            var blog = new Blog { Name = name };
            db.Blogs.Add(blog);
            db.SaveChanges();

            // Display all Blogs from the database
            var query = from b in db.Blogs
                        orderby b.Name
                        select b;

            Console.WriteLine("All blogs in the database:");
            foreach (var item in query)
            {
                Console.WriteLine(item.Name);
            }

            Console.WriteLine("Press any key to exit...");
            Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="2bce5-178">你现在可以运行该应用程序和它进行测试。</span><span class="sxs-lookup"><span data-stu-id="2bce5-178">You can now run the application and test it out.</span></span>

```
Enter a name for a new Blog: ADO.NET Blog
All blogs in the database:
ADO.NET Blog
Press any key to exit...
```
 

## <a name="5-dealing-with-database-changes"></a><span data-ttu-id="2bce5-179">5.处理数据库更改</span><span class="sxs-lookup"><span data-stu-id="2bce5-179">5. Dealing with Database Changes</span></span>

<span data-ttu-id="2bce5-180">现在就应该对我们的数据库架构进行一些更改，当我们进行这些更改，我们还需要更新我们的模型以反映这些更改。</span><span class="sxs-lookup"><span data-stu-id="2bce5-180">Now it’s time to make some changes to our database schema, when we make these changes we also need to update our model to reflect those changes.</span></span>

<span data-ttu-id="2bce5-181">第一步是对数据库架构进行某些更改。</span><span class="sxs-lookup"><span data-stu-id="2bce5-181">The first step is to make some changes to the database schema.</span></span> <span data-ttu-id="2bce5-182">我们要将用户表添加到架构。</span><span class="sxs-lookup"><span data-stu-id="2bce5-182">We’re going to add a Users table to the schema.</span></span>

-   <span data-ttu-id="2bce5-183">右键单击**DatabaseFirst.Blogging**数据库在服务器资源管理器并选择**新查询**</span><span class="sxs-lookup"><span data-stu-id="2bce5-183">Right-click on the **DatabaseFirst.Blogging** database in Server Explorer and select **New Query**</span></span>
-   <span data-ttu-id="2bce5-184">将下面的 SQL 复制到新的查询，然后右键单击查询并选择**Execute**</span><span class="sxs-lookup"><span data-stu-id="2bce5-184">Copy the following SQL into the new query, then right-click on the query and select **Execute**</span></span>

``` SQL
CREATE TABLE [dbo].[Users]
(
    [Username] NVARCHAR(50) NOT NULL PRIMARY KEY,  
    [DisplayName] NVARCHAR(MAX) NULL
)
```

<span data-ttu-id="2bce5-185">现在，将架构更新，就可以使用这些更改更新模型。</span><span class="sxs-lookup"><span data-stu-id="2bce5-185">Now that the schema is updated, it’s time to update the model with those changes.</span></span>

-   <span data-ttu-id="2bce5-186">右键单击某一空白点的 EF 设计器中您的模型并选择从数据库更新模型...，这将启动更新向导</span><span class="sxs-lookup"><span data-stu-id="2bce5-186">Right-click on an empty spot of your model in the EF Designer and select ‘Update Model from Database…’, this will launch the Update Wizard</span></span>
-   <span data-ttu-id="2bce5-187">在更新向导检查表旁边的框的添加选项卡上，这表示我们想要从架构中添加任何新表。</span><span class="sxs-lookup"><span data-stu-id="2bce5-187">On the Add tab of the Update Wizard check the box next to Tables, this indicates that we want to add any new tables from the schema.</span></span>
    <span data-ttu-id="2bce5-188">*刷新选项卡显示在更新期间将检查其进行更改的模型中的任何现有的表。删除选项卡显示已从架构中删除，并且将还在从模型期间删除更新的任何表。这两个选项卡上的信息自动检测并提供仅供参考之用，无法更改任何设置。*</span><span class="sxs-lookup"><span data-stu-id="2bce5-188">*The Refresh tab shows any existing tables in the model that will be checked for changes during the update. The Delete tabs show any tables that have been removed from the schema and will also be removed from the model as part of the update. The information on these two tabs is automatically detected and is provided for informational purposes only, you cannot change any settings.*</span></span>

    ![刷新向导](~/ef6/media/refreshwizard.png)

-   <span data-ttu-id="2bce5-190">单击完成上更新向导</span><span class="sxs-lookup"><span data-stu-id="2bce5-190">Click Finish on the Update Wizard</span></span>

 

<span data-ttu-id="2bce5-191">模型现在更新以包括新的用户实体映射到我们添加到数据库的用户表。</span><span class="sxs-lookup"><span data-stu-id="2bce5-191">The model is now updated to include a new User entity that maps to the Users table we added to the database.</span></span>

![模型更新](~/ef6/media/modelupdated.png)

## <a name="summary"></a><span data-ttu-id="2bce5-193">总结</span><span class="sxs-lookup"><span data-stu-id="2bce5-193">Summary</span></span>

<span data-ttu-id="2bce5-194">在本演练中，我们在第一个数据库开发，这使我们能够在 EF 设计器中基于现有数据库创建模型。</span><span class="sxs-lookup"><span data-stu-id="2bce5-194">In this walkthrough we looked at Database First development, which allowed us to create a model in the EF Designer based on an existing database.</span></span> <span data-ttu-id="2bce5-195">然后，使用该模型以读取和从数据库中写入一些数据。</span><span class="sxs-lookup"><span data-stu-id="2bce5-195">We then used that model to read and write some data from the database.</span></span> <span data-ttu-id="2bce5-196">最后，我们更新模型以反映我们对数据库架构所做的更改。</span><span class="sxs-lookup"><span data-stu-id="2bce5-196">Finally, we updated the model to reflect changes we made to the database schema.</span></span>
