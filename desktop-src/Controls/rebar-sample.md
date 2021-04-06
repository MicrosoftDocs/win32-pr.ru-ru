---
title: Образец главной панели
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: 'Дополнительные сведения о: Пример главной панели'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990382"
---
# <a name="rebar-sample"></a><span data-ttu-id="93620-103">Образец главной панели</span><span class="sxs-lookup"><span data-stu-id="93620-103">Rebar Sample</span></span>

<span data-ttu-id="93620-104">В этом разделе описывается пример кода главной панели.</span><span class="sxs-lookup"><span data-stu-id="93620-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="93620-105">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="93620-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="93620-106">Описание</span><span class="sxs-lookup"><span data-stu-id="93620-106">Description</span></span>](#description)
-   [<span data-ttu-id="93620-107">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="93620-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="93620-108">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="93620-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="93620-109">Создание примера</span><span class="sxs-lookup"><span data-stu-id="93620-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="93620-110">См. также</span><span class="sxs-lookup"><span data-stu-id="93620-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="93620-111">Описание</span><span class="sxs-lookup"><span data-stu-id="93620-111">Description</span></span>

<span data-ttu-id="93620-112">В образце главной панели показано, как реализовать простой общий элемент управления "Главная панель" в приложении.</span><span class="sxs-lookup"><span data-stu-id="93620-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="93620-113">В этом примере создается элемент управления "Главная панель" с двумя полосами.</span><span class="sxs-lookup"><span data-stu-id="93620-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="93620-114">Одна содержит поле со списком, а другая содержит кнопку.</span><span class="sxs-lookup"><span data-stu-id="93620-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="93620-115">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="93620-115">Minimum Requirements</span></span>



| <span data-ttu-id="93620-116">Продукт</span><span class="sxs-lookup"><span data-stu-id="93620-116">Product</span></span>          | <span data-ttu-id="93620-117">Version</span><span class="sxs-lookup"><span data-stu-id="93620-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="93620-118">DLL</span><span class="sxs-lookup"><span data-stu-id="93620-118">DLL</span></span>              | <span data-ttu-id="93620-119">comctl32.dll версии 4,71</span><span class="sxs-lookup"><span data-stu-id="93620-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="93620-120">Операционная система</span><span class="sxs-lookup"><span data-stu-id="93620-120">Operating System</span></span> | <span data-ttu-id="93620-121">Windows 95 с Internet Explorer 4,0</span><span class="sxs-lookup"><span data-stu-id="93620-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="93620-122">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="93620-122">Downloading the Sample</span></span>

<span data-ttu-id="93620-123">Образец главной панели устанавливается в составе [пакета средств разработки программного обеспечения (SDK) для Windows](https://msdn.microsoft.com/windows/bb980924.aspx) и доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="93620-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="93620-124">Расположение</span><span class="sxs-lookup"><span data-stu-id="93620-124">Location</span></span>    | <span data-ttu-id="93620-125">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="93620-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93620-126">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="93620-126">Windows SDK</span></span> | <span data-ttu-id="93620-127">% Program Files% \\ Microsoft \\ Windows SDK \\ \[ номер версии \] \\ примеры \\ винуи \\ элементы управления \\ Общая \\ Главная панель</span><span class="sxs-lookup"><span data-stu-id="93620-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="93620-128">Построение образца</span><span class="sxs-lookup"><span data-stu-id="93620-128">Building the Sample</span></span>

<span data-ttu-id="93620-129">Чтобы построить пример с помощью командной строки, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="93620-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="93620-130">Откройте окно командной строки и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="93620-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="93620-131">Введите `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="93620-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="93620-132">Чтобы построить пример с помощью Visual Studio, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="93620-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="93620-133">Откройте проводник Windows и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="93620-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="93620-134">Дважды щелкните значок VCPROJ-файла, чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="93620-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="93620-135">В меню **Сборка** выберите пункт **построить решение** , чтобы выполнить сборку решения.</span><span class="sxs-lookup"><span data-stu-id="93620-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93620-136">См. также</span><span class="sxs-lookup"><span data-stu-id="93620-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93620-137">Элементы управления главной панели</span><span class="sxs-lookup"><span data-stu-id="93620-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




