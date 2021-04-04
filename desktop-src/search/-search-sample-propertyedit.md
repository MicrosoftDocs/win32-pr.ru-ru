---
description: В примере кода Пропертедит показано, как преобразовать каноническое имя свойства в PROPERTYKEY, задать для хранилища свойств значение, равное значению элемента, и записать данные обратно в файловый поток.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896934"
---
# <a name="propertyedit"></a><span data-ttu-id="0ee5e-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="0ee5e-103">PropertyEdit</span></span>

<span data-ttu-id="0ee5e-104">В примере кода Пропертедит показано, как преобразовать каноническое имя свойства в PROPERTYKEY, задать для хранилища свойств значение, равное значению элемента, и записать данные обратно в файловый поток.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="0ee5e-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0ee5e-106">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee5e-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0ee5e-107">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0ee5e-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0ee5e-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="0ee5e-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0ee5e-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0ee5e-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0ee5e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0ee5e-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0ee5e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee5e-111">Requirements</span></span>



| <span data-ttu-id="0ee5e-112">Продукт</span><span class="sxs-lookup"><span data-stu-id="0ee5e-112">Product</span></span>     | <span data-ttu-id="0ee5e-113">Минимальная версия продукта</span><span class="sxs-lookup"><span data-stu-id="0ee5e-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="0ee5e-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0ee5e-114">Windows</span></span>     | <span data-ttu-id="0ee5e-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ee5e-115">Windows 7</span></span>               |
| <span data-ttu-id="0ee5e-116">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0ee5e-116">Windows SDK</span></span> | <span data-ttu-id="0ee5e-117">7.0</span><span class="sxs-lookup"><span data-stu-id="0ee5e-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0ee5e-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0ee5e-118">Downloading the Sample</span></span>

<span data-ttu-id="0ee5e-119">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="0ee5e-120">Расположение</span><span class="sxs-lookup"><span data-stu-id="0ee5e-120">Location</span></span>      | <span data-ttu-id="0ee5e-121">URL-адрес пути</span><span class="sxs-lookup"><span data-stu-id="0ee5e-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0ee5e-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="0ee5e-122">GitHub</span></span>  | [<span data-ttu-id="0ee5e-123">Пример Пропертедит</span><span class="sxs-lookup"><span data-stu-id="0ee5e-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="0ee5e-124">Для всех версий Windows, включая Windows 7, рекомендуется загрузить примеры непосредственно из GitHub, чтобы получить самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="0ee5e-125">Построение образца</span><span class="sxs-lookup"><span data-stu-id="0ee5e-125">Building the Sample</span></span>

<span data-ttu-id="0ee5e-126">Чтобы построить образец из командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0ee5e-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="0ee5e-127">Откройте окно командной строки и перейдите в каталог проекта **пропертедит** .</span><span class="sxs-lookup"><span data-stu-id="0ee5e-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="0ee5e-128">Введите `msbuild PropertyEdit.sln`.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="0ee5e-129">Чтобы создать пример с использованием Microsoft Visual Studio (предпочтительно):</span><span class="sxs-lookup"><span data-stu-id="0ee5e-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0ee5e-130">Откройте проводник Windows и перейдите в каталог проекта **пропертедит** .</span><span class="sxs-lookup"><span data-stu-id="0ee5e-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="0ee5e-131">Дважды щелкните значок файла Пропертедит. sln, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="0ee5e-132">Расширение имени файла. sln не отображается в разделе Параметры папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="0ee5e-133">В этом случае его можно определить по его уникальному значку или описанию типа "Microsoft Visual Studio решение".</span><span class="sxs-lookup"><span data-stu-id="0ee5e-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="0ee5e-134">В меню **Сборка** выберите пункт **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0ee5e-135">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0ee5e-135">Running the Sample</span></span>

1.  <span data-ttu-id="0ee5e-136">Перейдите в каталог, содержащий новый исполняемый файл, с помощью окна командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="0ee5e-137">В командной строке введите `PropertyEdit.exe` или в проводнике Windows дважды щелкните значок PropertyEdit.exe.</span><span class="sxs-lookup"><span data-stu-id="0ee5e-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ee5e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0ee5e-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0ee5e-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0ee5e-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0ee5e-140">Поиск примеров кода</span><span class="sxs-lookup"><span data-stu-id="0ee5e-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="0ee5e-141">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="0ee5e-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0ee5e-142">**ипропертисторе**</span><span class="sxs-lookup"><span data-stu-id="0ee5e-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="0ee5e-143">Сведения о свойствах и обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="0ee5e-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="0ee5e-144">[Схема описания свойства](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0ee5e-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 
