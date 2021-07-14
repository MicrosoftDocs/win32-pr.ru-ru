---
title: Пример коллекции
description: в этом примере кода демонстрируется разметка и код, необходимые для использования различных типов элементов управления галереи, входящих в состав платформы Windows Ribbon.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691753"
---
# <a name="gallery-sample"></a><span data-ttu-id="a30eb-103">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="a30eb-103">Gallery Sample</span></span>

<span data-ttu-id="a30eb-104">в этом примере кода демонстрируется разметка и код, необходимые для использования различных типов элементов управления галереи, входящих в состав платформы Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="a30eb-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="a30eb-105">Пример включает в себя код, который можно использовать для динамического заполнения элементов в коллекциях, а также для управления специальными событиями коллекции, которые поддерживают ориентированный на результаты пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a30eb-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="a30eb-106">Использование</span><span class="sxs-lookup"><span data-stu-id="a30eb-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="a30eb-107">Создание примера</span><span class="sxs-lookup"><span data-stu-id="a30eb-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="a30eb-108">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a30eb-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="a30eb-109">Поддержка</span><span class="sxs-lookup"><span data-stu-id="a30eb-109">Support</span></span>](#support)
- [<span data-ttu-id="a30eb-110">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="a30eb-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="a30eb-111">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a30eb-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="a30eb-112">Использование</span><span class="sxs-lookup"><span data-stu-id="a30eb-112">Usage</span></span>

<span data-ttu-id="a30eb-113">примеры платформы ленты Windows можно скачать в виде автономных Microsoft Visual Studio проектов из [центра загрузки майкрософт](https://www.microsoft.com/download/details.aspx?id=9620) или установить в составе [Windows пакета средств разработки программного обеспечения (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="a30eb-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="a30eb-114">Windows пакет средств разработки программного обеспечения (SDK) (стандартный путь установки):% ProgramFiles% \\ пакеты sdk майкрософт \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="a30eb-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="a30eb-115">Построение образца</span><span class="sxs-lookup"><span data-stu-id="a30eb-115">Building the Sample</span></span>

<span data-ttu-id="a30eb-116">Скачайте пример.</span><span class="sxs-lookup"><span data-stu-id="a30eb-116">Download the sample.</span></span>

<span data-ttu-id="a30eb-117">установите Windows SDK для Windows 7 и откройте командное окно среды сборки.</span><span class="sxs-lookup"><span data-stu-id="a30eb-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="a30eb-118">В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.</span><span class="sxs-lookup"><span data-stu-id="a30eb-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="a30eb-119">Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца.</span><span class="sxs-lookup"><span data-stu-id="a30eb-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="a30eb-120">В командной строке введите команду MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="a30eb-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="a30eb-121">Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.</span><span class="sxs-lookup"><span data-stu-id="a30eb-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="a30eb-122">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="a30eb-122">Running the Sample</span></span>

<span data-ttu-id="a30eb-123">Чтобы запустить пример из окна командной строки среды сборки, выполните .exe файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.</span><span class="sxs-lookup"><span data-stu-id="a30eb-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="a30eb-124">Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="a30eb-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="a30eb-125">Поддержка</span><span class="sxs-lookup"><span data-stu-id="a30eb-125">Support</span></span>

<span data-ttu-id="a30eb-126">на [форуме Windows ribbon](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задать вопросы, связанные с разработкой приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="a30eb-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="a30eb-127">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="a30eb-127">Minimum Requirements</span></span>



| <span data-ttu-id="a30eb-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a30eb-128">Requirement</span></span> | <span data-ttu-id="a30eb-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a30eb-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30eb-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a30eb-130">Minimum supported client</span></span> | <span data-ttu-id="a30eb-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a30eb-131">Windows 7</span></span><br/> <span data-ttu-id="a30eb-132">Windows vista с пакетом обновления 2 (sp2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="a30eb-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="a30eb-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a30eb-133">Minimum supported server</span></span> | <span data-ttu-id="a30eb-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a30eb-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="a30eb-135">Windows сервер 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="a30eb-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="a30eb-136">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a30eb-136">Windows SDK</span></span>              | <span data-ttu-id="a30eb-137">7.0</span><span class="sxs-lookup"><span data-stu-id="a30eb-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="a30eb-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a30eb-138">Visual Studio</span></span>            | <span data-ttu-id="a30eb-139">2008</span><span class="sxs-lookup"><span data-stu-id="a30eb-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="a30eb-140">Заголовочные и IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="a30eb-140">Header and IDL files</span></span>     | <span data-ttu-id="a30eb-141">уириббон. h, уириббон. idl</span><span class="sxs-lookup"><span data-stu-id="a30eb-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="a30eb-142">[обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows приложения ленты как Windows Vista, так и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a30eb-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a30eb-143">обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="a30eb-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="a30eb-144">сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , Центр обновления Windows могут определить, установлено ли необходимое обновление. если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a30eb-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a30eb-145">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a30eb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a30eb-146">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="a30eb-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="a30eb-147">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="a30eb-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="a30eb-148">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="a30eb-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="a30eb-149">Коллекция на ленте</span><span class="sxs-lookup"><span data-stu-id="a30eb-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="a30eb-150">Коллекция разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="a30eb-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="a30eb-151">Свойства коллекции</span><span class="sxs-lookup"><span data-stu-id="a30eb-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





