---
title: Разработка приложения OEM, использующего пользовательский файл
description: Узнайте, как разработать приложение, использующее пользовательский файл для передачи сведений от изготовителя оборудования в приложение.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105700839"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="e81d7-103">Разработка приложения OEM, использующего пользовательский файл</span><span class="sxs-lookup"><span data-stu-id="e81d7-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="e81d7-104">Дополнительные сведения о создании и использовании пользовательских файлов данных см. в разделе [параметры Command-Line обслуживания пакета приложения DISM (. appx или. appxbundle)](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span><span class="sxs-lookup"><span data-stu-id="e81d7-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="e81d7-105">Узнайте, как разработать приложение, использующее пользовательский файл для передачи сведений от изготовителя оборудования в приложение.</span><span class="sxs-lookup"><span data-stu-id="e81d7-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="e81d7-106">Для приложений, создаваемых для развертывания изготовителем оборудования, можно использовать пользовательский файл для передачи сведений от изготовителя оборудования в приложения.</span><span class="sxs-lookup"><span data-stu-id="e81d7-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="e81d7-107">Чтобы передать сведения об ИЗГОТОВИТЕЛе в приложение, создайте файл Custom. Data в папке microsoft.sysTEM. Package. метаданных.</span><span class="sxs-lookup"><span data-stu-id="e81d7-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="e81d7-108">Это имя файла является специальным для операционной системы и автоматически переносится во время обновления операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e81d7-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="e81d7-109">Поставщики вычислительной техники могут использовать этот файл для передачи настраиваемых идентификаторов, чтобы приложения были осведомлены о развертывании их изготовителями оборудования.</span><span class="sxs-lookup"><span data-stu-id="e81d7-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="e81d7-110">У вас может быть только один настраиваемый файл. Data для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="e81d7-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="e81d7-111">Приложения должны иметь возможность правильно искать и считывать этот файл.</span><span class="sxs-lookup"><span data-stu-id="e81d7-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="e81d7-112">Разработчики считают файл ненадежным.</span><span class="sxs-lookup"><span data-stu-id="e81d7-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e81d7-113">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e81d7-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e81d7-114">Технологии</span><span class="sxs-lookup"><span data-stu-id="e81d7-114">Technologies</span></span>

-   [<span data-ttu-id="e81d7-115">Краткое руководство. запрос сведений о манифесте пакета приложения</span><span class="sxs-lookup"><span data-stu-id="e81d7-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="e81d7-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e81d7-116">Prerequisites</span></span>

-   <span data-ttu-id="e81d7-117">Для добавления пакета приложения с пользовательским файлом данных требуется средство [обслуживания образов развертывания и управления ими (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) .</span><span class="sxs-lookup"><span data-stu-id="e81d7-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="e81d7-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e81d7-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="e81d7-119">Шаг 1. Создание пользовательского файла и добавление его в папку метаданных пакета</span><span class="sxs-lookup"><span data-stu-id="e81d7-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="e81d7-120">Вы можете спроектировать приложение для использования любого формата, выбранного для пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="e81d7-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="e81d7-121">Например, можно использовать XML, текстовый файл или другой тип файла для организации данных.</span><span class="sxs-lookup"><span data-stu-id="e81d7-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="e81d7-122">Рекомендуется продумать, как можно проверить и проверить файл.</span><span class="sxs-lookup"><span data-stu-id="e81d7-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="e81d7-123">Например, можно создать схему XML для проверки XML-файла.</span><span class="sxs-lookup"><span data-stu-id="e81d7-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="e81d7-124">Можно указать любой тип файла с любым именем файла для пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="e81d7-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="e81d7-125">При добавлении пакета приложения с пользовательским файлом данных с помощью средства [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) система DISM переименовывает пользовательский файл в Custom. Data и сохраняет его в папку microsoft.sysTEM. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="e81d7-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="e81d7-126">Приложение не может изменить пользовательский файл данных.</span><span class="sxs-lookup"><span data-stu-id="e81d7-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="e81d7-127">Это ресурс только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e81d7-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="e81d7-128">Шаг 2. доступ к пользовательскому файлу данных для приложения</span><span class="sxs-lookup"><span data-stu-id="e81d7-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="e81d7-129">Чтобы получить сведения о текущем пакете, можно получить доступ к пользовательскому файлу. Data для приложения из вашего кода с помощью API-интерфейсов Windows.</span><span class="sxs-lookup"><span data-stu-id="e81d7-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="e81d7-130">Пример:</span><span class="sxs-lookup"><span data-stu-id="e81d7-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="e81d7-131">Дополнительные сведения о разработке с помощью свойства [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) см. в разделе [Краткое руководство: запрос сведений о манифесте пакета приложения](how-to-query-package-identity-information.md).</span><span class="sxs-lookup"><span data-stu-id="e81d7-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="e81d7-132">Дополнительные сведения о доступе к файлу Custom. Data через [**исторажефолдер. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) и с помощью объектов [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) см. в разделе [доступ к данным и файлам](/previous-versions/windows/apps/hh464959(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="e81d7-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e81d7-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e81d7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e81d7-134">Краткое руководство. запрос сведений о манифесте пакета приложения</span><span class="sxs-lookup"><span data-stu-id="e81d7-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 