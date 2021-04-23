---
title: Пример свойства
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Дополнительные сведения: пример свойства'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140970"
---
# <a name="property-sample"></a><span data-ttu-id="ca1d4-103">Пример свойства</span><span class="sxs-lookup"><span data-stu-id="ca1d4-103">Property Sample</span></span>

<span data-ttu-id="ca1d4-104">В этом разделе описывается пример кода свойства.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="ca1d4-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="ca1d4-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="ca1d4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ca1d4-106">Description</span></span>](#description)
-   [<span data-ttu-id="ca1d4-107">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="ca1d4-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="ca1d4-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="ca1d4-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ca1d4-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="ca1d4-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ca1d4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ca1d4-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ca1d4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ca1d4-111">Description</span></span>

<span data-ttu-id="ca1d4-112">В примере свойства показано, как реализовать три различных стиля страниц свойств: модальный, немодальный и мастер.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="ca1d4-113">В нем также показано, как с помощью функции [*пропшитпрок*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) изменить диалоговое окно страницы свойств до или после его создания.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="ca1d4-114">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="ca1d4-114">Minimum Requirements</span></span>



| <span data-ttu-id="ca1d4-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="ca1d4-115">Product</span></span>          | <span data-ttu-id="ca1d4-116">Version</span><span class="sxs-lookup"><span data-stu-id="ca1d4-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="ca1d4-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ca1d4-117">DLL</span></span>              | <span data-ttu-id="ca1d4-118">comctl32.dll версии 4,0</span><span class="sxs-lookup"><span data-stu-id="ca1d4-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="ca1d4-119">Операционная система</span><span class="sxs-lookup"><span data-stu-id="ca1d4-119">Operating System</span></span> | <span data-ttu-id="ca1d4-120">Windows 95, Microsoft Windows NT 3,1</span><span class="sxs-lookup"><span data-stu-id="ca1d4-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ca1d4-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="ca1d4-121">Downloading the Sample</span></span>

<span data-ttu-id="ca1d4-122">Пример свойства устанавливается как часть [пакета средств разработки программного обеспечения (SDK) для Windows](https://msdn.microsoft.com/windows/bb980924.aspx) и доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="ca1d4-123">Расположение</span><span class="sxs-lookup"><span data-stu-id="ca1d4-123">Location</span></span>    | <span data-ttu-id="ca1d4-124">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="ca1d4-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1d4-125">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ca1d4-125">Windows SDK</span></span> | <span data-ttu-id="ca1d4-126">% Program Files% \\ Microsoft \\ Windows SDK \\ \[ номер версии \] \\ примеры \\ винуи \\ элементы управления \\ Общие \\ Свойства</span><span class="sxs-lookup"><span data-stu-id="ca1d4-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="ca1d4-127">Построение образца</span><span class="sxs-lookup"><span data-stu-id="ca1d4-127">Building the Sample</span></span>

<span data-ttu-id="ca1d4-128">Чтобы построить пример с помощью командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ca1d4-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="ca1d4-129">Откройте окно командной строки и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="ca1d4-130">Введите `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="ca1d4-131">Чтобы построить пример с помощью Visual Studio, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ca1d4-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="ca1d4-132">Откройте проводник Windows и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="ca1d4-133">Дважды щелкните значок VCPROJ-файла, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="ca1d4-134">В меню **Сборка** выберите пункт **построить решение** , чтобы выполнить сборку решения.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca1d4-135">См. также</span><span class="sxs-lookup"><span data-stu-id="ca1d4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca1d4-136">О страницах свойств</span><span class="sxs-lookup"><span data-stu-id="ca1d4-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 




