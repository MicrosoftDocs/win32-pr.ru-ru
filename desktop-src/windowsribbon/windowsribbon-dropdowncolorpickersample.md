---
title: Пример Дропдовнколорпиккер
description: в этом примере кода демонстрируется разметка и код, необходимые для использования элемента управления дропдовнколорпиккер ленты Windows.
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 0bb4cb91fdcd5450bd9be5ee70a8ca6c0fe253f6
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691693"
---
# <a name="dropdowncolorpicker-sample"></a><span data-ttu-id="6bbe4-103">Пример Дропдовнколорпиккер</span><span class="sxs-lookup"><span data-stu-id="6bbe4-103">DropDownColorPicker Sample</span></span>

<span data-ttu-id="6bbe4-104">в этом примере кода демонстрируется разметка и код, необходимые для использования элемента управления дропдовнколорпиккер ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-104">This code sample demonstrates the markup and code required to use a Windows Ribbon DropDownColorPicker control.</span></span>

- [<span data-ttu-id="6bbe4-105">Использование</span><span class="sxs-lookup"><span data-stu-id="6bbe4-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="6bbe4-106">Создание примера</span><span class="sxs-lookup"><span data-stu-id="6bbe4-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="6bbe4-107">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="6bbe4-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="6bbe4-108">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6bbe4-108">Support</span></span>](#support)
- [<span data-ttu-id="6bbe4-109">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="6bbe4-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="6bbe4-110">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="6bbe4-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="6bbe4-111">Использование</span><span class="sxs-lookup"><span data-stu-id="6bbe4-111">Usage</span></span>

<span data-ttu-id="6bbe4-112">примеры платформы ленты Windows можно скачать в виде автономных Microsoft Visual Studio проектов из [центра загрузки майкрософт](https://www.microsoft.com/download/details.aspx?id=9620) или установить в составе [Windows пакета средств разработки программного обеспечения (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="6bbe4-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="6bbe4-113">Windows пакет средств разработки программного обеспечения (SDK) (стандартный путь установки):% ProgramFiles% \\ пакеты sdk майкрософт \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ дропдовнколорпиккер</span><span class="sxs-lookup"><span data-stu-id="6bbe4-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\DropDownColorPicker</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="6bbe4-114">Построение образца</span><span class="sxs-lookup"><span data-stu-id="6bbe4-114">Building the Sample</span></span>

<span data-ttu-id="6bbe4-115">Скачайте пример.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-115">Download the sample.</span></span>

<span data-ttu-id="6bbe4-116">установите Windows SDK для Windows 7 и откройте командное окно среды сборки.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="6bbe4-117">В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="6bbe4-118">Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="6bbe4-119">В командной строке введите команду MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="6bbe4-120">Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="6bbe4-121">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="6bbe4-121">Running the Sample</span></span>

<span data-ttu-id="6bbe4-122">Чтобы запустить пример из окна командной строки среды сборки, выполните .exe файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="6bbe4-123">Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="6bbe4-124">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6bbe4-124">Support</span></span>

<span data-ttu-id="6bbe4-125">на [форуме Windows ribbon](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задать вопросы, связанные с разработкой приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="6bbe4-126">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="6bbe4-126">Minimum Requirements</span></span>



| <span data-ttu-id="6bbe4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6bbe4-127">Requirement</span></span> | <span data-ttu-id="6bbe4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6bbe4-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbe4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bbe4-129">Minimum supported client</span></span> | <span data-ttu-id="6bbe4-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6bbe4-130">Windows 7</span></span><br/> <span data-ttu-id="6bbe4-131">Windows vista с пакетом обновления 2 (sp2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bbe4-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="6bbe4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bbe4-132">Minimum supported server</span></span> | <span data-ttu-id="6bbe4-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6bbe4-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="6bbe4-134">Windows сервер 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bbe4-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="6bbe4-135">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6bbe4-135">Windows SDK</span></span>              | <span data-ttu-id="6bbe4-136">7.0</span><span class="sxs-lookup"><span data-stu-id="6bbe4-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="6bbe4-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6bbe4-137">Visual Studio</span></span>            | <span data-ttu-id="6bbe4-138">2008</span><span class="sxs-lookup"><span data-stu-id="6bbe4-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="6bbe4-139">Заголовочные и IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="6bbe4-139">Header and IDL files</span></span>     | <span data-ttu-id="6bbe4-140">уириббон. h, уириббон. idl</span><span class="sxs-lookup"><span data-stu-id="6bbe4-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="6bbe4-141">[обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows приложения ленты как Windows Vista, так и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6bbe4-142">обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="6bbe4-143">сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , Центр обновления Windows могут определить, установлено ли необходимое обновление. если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6bbe4-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6bbe4-144">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="6bbe4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bbe4-145">Выбор цвета для раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="6bbe4-145">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="6bbe4-146">Свойства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="6bbe4-146">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





