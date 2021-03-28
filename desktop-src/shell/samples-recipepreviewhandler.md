---
description: Демонстрирует написание обработчика, используемого для отображения предварительного просмотра файла в панели предварительного просмотра проводника Windows или других узлов обработчика просмотра.
title: 'Пример: обработчик просмотра рецепта'
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985784"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="096d8-103">Пример: обработчик просмотра рецепта</span><span class="sxs-lookup"><span data-stu-id="096d8-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="096d8-104">Демонстрирует написание обработчика, используемого для отображения предварительного просмотра файла в панели предварительного просмотра проводника Windows или других узлов обработчика просмотра.</span><span class="sxs-lookup"><span data-stu-id="096d8-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="096d8-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="096d8-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="096d8-106">Требования</span><span class="sxs-lookup"><span data-stu-id="096d8-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="096d8-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="096d8-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="096d8-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="096d8-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="096d8-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="096d8-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="096d8-110">Отмена регистрации библиотеки DLL обработчика просмотра примера</span><span class="sxs-lookup"><span data-stu-id="096d8-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="096d8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="096d8-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="096d8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="096d8-112">Requirements</span></span>



| <span data-ttu-id="096d8-113">Продукт</span><span class="sxs-lookup"><span data-stu-id="096d8-113">Product</span></span>                                | <span data-ttu-id="096d8-114">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="096d8-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="096d8-115">Windows</span><span class="sxs-lookup"><span data-stu-id="096d8-115">Windows</span></span>                                | <span data-ttu-id="096d8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="096d8-116">Windows Vista</span></span>           |
| <span data-ttu-id="096d8-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="096d8-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="096d8-118">7.0</span><span class="sxs-lookup"><span data-stu-id="096d8-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="096d8-119">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="096d8-119">Downloading the Sample</span></span>

| <span data-ttu-id="096d8-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="096d8-120">Location</span></span>      | <span data-ttu-id="096d8-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="096d8-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="096d8-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="096d8-122">GitHub</span></span>  | [<span data-ttu-id="096d8-123">Пример РеЦипепревиевхандлер</span><span class="sxs-lookup"><span data-stu-id="096d8-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="096d8-124">Построение образца</span><span class="sxs-lookup"><span data-stu-id="096d8-124">Building the Sample</span></span>

<span data-ttu-id="096d8-125">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="096d8-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="096d8-126">Откройте окно командной строки и перейдите в каталог проекта **реЦипепревиевхандлер** .</span><span class="sxs-lookup"><span data-stu-id="096d8-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="096d8-127">Например, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="096d8-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="096d8-128">Введите `msbuild PreviewHandlerSDKSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="096d8-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="096d8-129">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="096d8-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="096d8-130">Откройте проводник Windows и перейдите в каталог проекта **реЦипепревиевхандлер** .</span><span class="sxs-lookup"><span data-stu-id="096d8-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="096d8-131">Дважды щелкните значок файла Превиевхандлерсдксампле. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="096d8-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="096d8-132">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="096d8-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="096d8-133">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="096d8-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="096d8-134">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="096d8-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="096d8-135">Если целевой системой является 64-разрядный (x64), этот пример обработчика просмотра должен быть построен как 64-разрядное приложение.</span><span class="sxs-lookup"><span data-stu-id="096d8-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="096d8-136">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="096d8-136">Running the Sample</span></span>

1.  <span data-ttu-id="096d8-137">Откройте окно командной строки и перейдите к созданному каталогу проекта **реЦипепревиевхандлер** .</span><span class="sxs-lookup"><span data-stu-id="096d8-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="096d8-138">Например, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="096d8-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="096d8-139">Введите `regsvr32.exe PreviewHandlerSDKSample.dll` , чтобы зарегистрировать обработчик.</span><span class="sxs-lookup"><span data-stu-id="096d8-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="096d8-140">Откройте проводник Windows и отобразите панель предварительного просмотра, если она еще не отображается.</span><span class="sxs-lookup"><span data-stu-id="096d8-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="096d8-141">**Windows 7**. Нажмите кнопку панели предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="096d8-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="096d8-142">**Windows Vista**. Щелкните меню **Упорядочить** , перейдите в подменю **Макет** и выберите **область просмотра**.</span><span class="sxs-lookup"><span data-stu-id="096d8-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="096d8-143">С помощью проводника Windows перейдите в каталог проекта **реЦипепревиевхандлер** .</span><span class="sxs-lookup"><span data-stu-id="096d8-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="096d8-144">Выберите файл example. рецепт.</span><span class="sxs-lookup"><span data-stu-id="096d8-144">Select the example .recipe file.</span></span>

<span data-ttu-id="096d8-145">Чтобы оба 32-разрядных (x86) и 64-разрядных (x64) выходных данных работали в 64-разрядной версии Windows, установите значение **AppID** на суррогатный узел WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="096d8-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="096d8-146">Отмена регистрации библиотеки DLL обработчика просмотра примера</span><span class="sxs-lookup"><span data-stu-id="096d8-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="096d8-147">Откройте окно командной строки и введите, `regsvr32.exe /u PreviewHandlerSDKSample.dll` чтобы отменить регистрацию обработчика.</span><span class="sxs-lookup"><span data-stu-id="096d8-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="096d8-148">См. также</span><span class="sxs-lookup"><span data-stu-id="096d8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="096d8-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="096d8-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="096d8-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="096d8-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="096d8-151">Идентификаторы модели пользователя приложения (Аппусермоделидс)</span><span class="sxs-lookup"><span data-stu-id="096d8-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
