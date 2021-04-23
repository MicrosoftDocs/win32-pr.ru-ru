---
title: Пример Кустомакксервер
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412611"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="15924-103">Пример Кустомакксервер</span><span class="sxs-lookup"><span data-stu-id="15924-103">CustomAccServer Sample</span></span>

<span data-ttu-id="15924-104">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="15924-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="15924-105">Описание</span><span class="sxs-lookup"><span data-stu-id="15924-105">Description</span></span>](#description)
-   [<span data-ttu-id="15924-106">Сведения о загрузке</span><span class="sxs-lookup"><span data-stu-id="15924-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="15924-107">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="15924-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="15924-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="15924-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="15924-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="15924-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="15924-110">См. также</span><span class="sxs-lookup"><span data-stu-id="15924-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="15924-111">Описание</span><span class="sxs-lookup"><span data-stu-id="15924-111">Description</span></span>

<span data-ttu-id="15924-112">В этом примере показано, как реализовать сервер Microsoft Active Accessibility для простого пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="15924-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="15924-113">Доступный объект для элемента управления состоит из корневого элемента (списка) и его потомков (элементов списка).</span><span class="sxs-lookup"><span data-stu-id="15924-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="15924-114">Сведения о загрузке</span><span class="sxs-lookup"><span data-stu-id="15924-114">Download Information</span></span>

<span data-ttu-id="15924-115">Пример Кустомакксервер устанавливается как часть [пакета средств разработки программного обеспечения Microsoft Windows (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) и доступен в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="15924-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="15924-116">Расположение</span><span class="sxs-lookup"><span data-stu-id="15924-116">Location</span></span>    | <span data-ttu-id="15924-117">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="15924-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15924-118">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="15924-118">Windows SDK</span></span> | <span data-ttu-id="15924-119">% Program Files% \\ Microsoft SDK \\ версии Windows — \\ \[ \] \\ примеры \\ винуи \\ MSAA</span><span class="sxs-lookup"><span data-stu-id="15924-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="15924-120">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="15924-120">Minimum Requirements</span></span>



| <span data-ttu-id="15924-121">Продукт</span><span class="sxs-lookup"><span data-stu-id="15924-121">Product</span></span>          | <span data-ttu-id="15924-122">Версия</span><span class="sxs-lookup"><span data-stu-id="15924-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="15924-123">Операционная система</span><span class="sxs-lookup"><span data-stu-id="15924-123">Operating System</span></span> | <span data-ttu-id="15924-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15924-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="15924-125">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="15924-125">Windows SDK</span></span>      | <span data-ttu-id="15924-126">7.0</span><span class="sxs-lookup"><span data-stu-id="15924-126">7.0</span></span>                             |
| <span data-ttu-id="15924-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="15924-127">Visual Studio</span></span>    | <span data-ttu-id="15924-128">2008</span><span class="sxs-lookup"><span data-stu-id="15924-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="15924-129">Построение образца</span><span class="sxs-lookup"><span data-stu-id="15924-129">Building the Sample</span></span>

<span data-ttu-id="15924-130">Чтобы построить пример с помощью Visual Studio 2008, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15924-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="15924-131">Запустите средство настройки пакета средств разработки программного обеспечения (SDK) для Microsoft Windows, поставляемое вместе с пакетом SDK, чтобы добавить в Visual Studio каталоги включения пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="15924-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="15924-132">Откройте проводник Windows и перейдите в каталог проекта.</span><span class="sxs-lookup"><span data-stu-id="15924-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="15924-133">Дважды щелкните значок файла. sln (решение), чтобы открыть проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="15924-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="15924-134">В меню **Сборка** выберите пункт **построить решение** , чтобы выполнить сборку решения.</span><span class="sxs-lookup"><span data-stu-id="15924-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="15924-135">Приложение будет построено в \\ каталоге отладки или выпуска по умолчанию \\ .</span><span class="sxs-lookup"><span data-stu-id="15924-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="15924-136">Чтобы построить пример из командной строки, см. раздел Создание образцов в заметках о выпуске Windows SDK в следующем расположении:% Program Files% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="15924-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="15924-137">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="15924-137">Running the Sample</span></span>

<span data-ttu-id="15924-138">Запуск примера:</span><span class="sxs-lookup"><span data-stu-id="15924-138">To run the sample:</span></span>

1.  <span data-ttu-id="15924-139">Перейдите в каталог, содержащий новый исполняемый файл, с помощью командной строки или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="15924-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="15924-140">Введите AccServer.exe в командной строке или дважды щелкните значок AccServer.exe, чтобы запустить его из проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="15924-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="15924-141">Чтобы запустить из Visual Studio, нажмите клавишу F5 или выберите команду **начать отладку** в меню **Отладка** .</span><span class="sxs-lookup"><span data-stu-id="15924-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15924-142">См. также</span><span class="sxs-lookup"><span data-stu-id="15924-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15924-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="15924-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




