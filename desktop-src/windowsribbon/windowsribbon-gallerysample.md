---
title: Пример коллекции
description: В этом примере кода демонстрируется разметка и код, необходимые для использования различных типов элементов управления галереи, входящих в платформу Windows Ribbon.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135375"
---
# <a name="gallery-sample"></a><span data-ttu-id="6fb59-103">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="6fb59-103">Gallery Sample</span></span>

<span data-ttu-id="6fb59-104">В этом примере кода демонстрируется разметка и код, необходимые для использования различных типов элементов управления галереи, входящих в платформу Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="6fb59-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="6fb59-105">Пример включает в себя код, который можно использовать для динамического заполнения элементов в коллекциях, а также для управления специальными событиями коллекции, которые поддерживают ориентированный на результаты пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6fb59-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

-   [<span data-ttu-id="6fb59-106">Использование</span><span class="sxs-lookup"><span data-stu-id="6fb59-106">Usage</span></span>](#usage)
    -   [<span data-ttu-id="6fb59-107">Создание примера</span><span class="sxs-lookup"><span data-stu-id="6fb59-107">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="6fb59-108">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="6fb59-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="6fb59-109">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6fb59-109">Support</span></span>](#support)
-   [<span data-ttu-id="6fb59-110">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="6fb59-110">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="6fb59-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6fb59-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="6fb59-112">Использование</span><span class="sxs-lookup"><span data-stu-id="6fb59-112">Usage</span></span>

<span data-ttu-id="6fb59-113">Образец коллекции можно скачать в виде автономного Microsoft Visual Studio проекта из [центра загрузки Майкрософт](https://www.microsoft.com/DOWNLOADS/en/default.aspx) или установленного в составе [пакета средств разработки программного обеспечения (SDK) для Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fb59-113">The Gallery Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="6fb59-114">Центр загрузки Майкрософт: [примеры для ленты Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="6fb59-114">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="6fb59-115">Пакет средств разработки программного обеспечения (SDK) для Windows (стандартный путь установки):% ProgramFiles% \\ пакеты SDK Microsoft \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="6fb59-115">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="6fb59-116">Построение образца</span><span class="sxs-lookup"><span data-stu-id="6fb59-116">Building the Sample</span></span>

<span data-ttu-id="6fb59-117">Загрузите пример на жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="6fb59-117">Download the sample to your hard disk.</span></span>

<span data-ttu-id="6fb59-118">Установите Windows SDK для Windows 7 и Откройте командное окно среды сборки.</span><span class="sxs-lookup"><span data-stu-id="6fb59-118">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="6fb59-119">В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.</span><span class="sxs-lookup"><span data-stu-id="6fb59-119">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="6fb59-120">Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца.</span><span class="sxs-lookup"><span data-stu-id="6fb59-120">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="6fb59-121">В командной строке введите команду MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="6fb59-121">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="6fb59-122">Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.</span><span class="sxs-lookup"><span data-stu-id="6fb59-122">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="6fb59-123">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="6fb59-123">Running the Sample</span></span>

<span data-ttu-id="6fb59-124">Чтобы запустить пример из командного окна среды сборки, выполните EXE файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.</span><span class="sxs-lookup"><span data-stu-id="6fb59-124">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="6fb59-125">Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="6fb59-125">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="6fb59-126">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6fb59-126">Support</span></span>

<span data-ttu-id="6fb59-127">На [форуме по разработке ленты Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задавать вопросы, связанные с разработкой приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="6fb59-127">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="6fb59-128">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="6fb59-128">Minimum Requirements</span></span>



| <span data-ttu-id="6fb59-129">Требование</span><span class="sxs-lookup"><span data-stu-id="6fb59-129">Requirement</span></span> | <span data-ttu-id="6fb59-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6fb59-130">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb59-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fb59-131">Minimum supported client</span></span> | <span data-ttu-id="6fb59-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fb59-132">Windows 7</span></span><br/> <span data-ttu-id="6fb59-133">Windows Vista с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fb59-133">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="6fb59-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fb59-134">Minimum supported server</span></span> | <span data-ttu-id="6fb59-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fb59-135">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="6fb59-136">Windows Server 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fb59-136">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="6fb59-137">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6fb59-137">Windows SDK</span></span>              | <span data-ttu-id="6fb59-138">7.0</span><span class="sxs-lookup"><span data-stu-id="6fb59-138">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="6fb59-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6fb59-139">Visual Studio</span></span>            | <span data-ttu-id="6fb59-140">2008</span><span class="sxs-lookup"><span data-stu-id="6fb59-140">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="6fb59-141">Заголовочные и IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="6fb59-141">Header and IDL files</span></span>     | <span data-ttu-id="6fb59-142">уириббон. h, уириббон. idl</span><span class="sxs-lookup"><span data-stu-id="6fb59-142">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="6fb59-143">[Обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows vista и Windows Server 2008 для приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="6fb59-143">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6fb59-144">Обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="6fb59-144">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="6fb59-145">Сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , могут иметь центр обновления Windows определить, установлена ли требуемая обновленная система. Если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6fb59-145">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6fb59-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6fb59-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb59-147">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="6fb59-147">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="6fb59-148">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="6fb59-148">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="6fb59-149">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="6fb59-149">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="6fb59-150">Коллекция на ленте</span><span class="sxs-lookup"><span data-stu-id="6fb59-150">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="6fb59-151">Коллекция разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="6fb59-151">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="6fb59-152">Свойства коллекции</span><span class="sxs-lookup"><span data-stu-id="6fb59-152">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





