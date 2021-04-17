---
title: Пример Влиствв
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Дополнительные сведения о: Влиствв Sample'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655983"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="a5255-103">Пример Влиствв</span><span class="sxs-lookup"><span data-stu-id="a5255-103">VListVW Sample</span></span>

<span data-ttu-id="a5255-104">В этом разделе описывается пример образца кода Влиствв.</span><span class="sxs-lookup"><span data-stu-id="a5255-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="a5255-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="a5255-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="a5255-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a5255-106">Description</span></span>](#description)
-   [<span data-ttu-id="a5255-107">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="a5255-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="a5255-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a5255-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a5255-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="a5255-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a5255-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a5255-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="a5255-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a5255-111">Description</span></span>

<span data-ttu-id="a5255-112">В примере Влиствв показано, как реализовать простой виртуальный элемент управления "представление списка" в приложении.</span><span class="sxs-lookup"><span data-stu-id="a5255-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="a5255-113">Виртуальный элемент управления "список" — это стандартный элемент управления "представление списка" с стилем **LVS \_ овнердата** .</span><span class="sxs-lookup"><span data-stu-id="a5255-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="a5255-114">В этом примере создается элемент управления "представление списка", в котором «виртуальная» содержит 100 000 элементов.</span><span class="sxs-lookup"><span data-stu-id="a5255-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="a5255-115">Элементы никогда не добавляются.</span><span class="sxs-lookup"><span data-stu-id="a5255-115">The items are never actually added.</span></span> <span data-ttu-id="a5255-116">Вместо этого виртуальный элемент управления "представление списка" — это количество элементов, содержащихся в сообщении [**LVM \_ сетитемкаунт**](lvm-setitemcount.md) .</span><span class="sxs-lookup"><span data-stu-id="a5255-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="a5255-117">При необходимости прорисовки элемента элемент управления "представление списка" запрашивает родительское окно для отображения информации с уведомлением [ЛВН \_ жетдиспинфо](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a5255-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="a5255-118">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="a5255-118">Minimum Requirements</span></span>



| <span data-ttu-id="a5255-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="a5255-119">Product</span></span>          | <span data-ttu-id="a5255-120">Version</span><span class="sxs-lookup"><span data-stu-id="a5255-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="a5255-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a5255-121">DLL</span></span>              | <span data-ttu-id="a5255-122">comctl32.dll версии 4,70</span><span class="sxs-lookup"><span data-stu-id="a5255-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="a5255-123">Операционная система</span><span class="sxs-lookup"><span data-stu-id="a5255-123">Operating System</span></span> | <span data-ttu-id="a5255-124">Windows 95, Microsoft Windows NT 3,51</span><span class="sxs-lookup"><span data-stu-id="a5255-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a5255-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="a5255-125">Downloading the Sample</span></span>

<span data-ttu-id="a5255-126">Пример Влиствв доступен на сайте GitHub в [репозитории классической выборки Windows](https://github.com/microsoft/Windows-classic-samples).</span><span class="sxs-lookup"><span data-stu-id="a5255-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="a5255-127">Примеры элементов управления "представление списка" можно найти [здесь](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw) .</span><span class="sxs-lookup"><span data-stu-id="a5255-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="a5255-128">Построение образца</span><span class="sxs-lookup"><span data-stu-id="a5255-128">Building the Sample</span></span>

<span data-ttu-id="a5255-129">Чтобы построить пример с помощью командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a5255-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="a5255-130">Откройте окно командной строки и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="a5255-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="a5255-131">Введите `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="a5255-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="a5255-132">Чтобы построить пример с помощью Visual Studio, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="a5255-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="a5255-133">Откройте проводник Windows и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="a5255-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="a5255-134">Дважды щелкните значок VCPROJ-файла, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a5255-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="a5255-135">В меню **Сборка** выберите пункт **построить решение** , чтобы выполнить сборку решения.</span><span class="sxs-lookup"><span data-stu-id="a5255-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5255-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a5255-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5255-137">Сведения об элементах управления List-View</span><span class="sxs-lookup"><span data-stu-id="a5255-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




