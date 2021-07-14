---
title: Пример Хтмледитриббон
description: в этом образце кода показана разметка и код, необходимые для переноса существующего Microsoft Foundation Classesного приложения (MFC) для использования ленты Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691713"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="4d828-103">Пример Хтмледитриббон</span><span class="sxs-lookup"><span data-stu-id="4d828-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="4d828-104">в этом образце кода показана разметка и код, необходимые для переноса существующего Microsoft Foundation Classesного приложения (MFC) для использования ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="4d828-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="4d828-105">он был создан с помощью существующего примера приложения MFC хтмледит и изменения его кода и ресурсов для использования ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="4d828-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

- [<span data-ttu-id="4d828-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d828-106">Remarks</span></span>](#remarks)
- [<span data-ttu-id="4d828-107">Использование</span><span class="sxs-lookup"><span data-stu-id="4d828-107">Usage</span></span>](#usage)
  - [<span data-ttu-id="4d828-108">Создание примера</span><span class="sxs-lookup"><span data-stu-id="4d828-108">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="4d828-109">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="4d828-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="4d828-110">Поддержка</span><span class="sxs-lookup"><span data-stu-id="4d828-110">Support</span></span>](#support)
- [<span data-ttu-id="4d828-111">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="4d828-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="4d828-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d828-112">Remarks</span></span>

<span data-ttu-id="4d828-113">Пример для MFC см. в разделе [Хтмледит Sample: заключает в оболочку элемент управления редактированием в Internet Explorer MSHTML](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="4d828-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="4d828-114">Использование</span><span class="sxs-lookup"><span data-stu-id="4d828-114">Usage</span></span>

<span data-ttu-id="4d828-115">примеры платформы ленты Windows можно скачать в виде автономных Microsoft Visual Studio проектов из [центра загрузки майкрософт](https://www.microsoft.com/download/details.aspx?id=9620) или установить в составе [Windows пакета средств разработки программного обеспечения (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="4d828-115">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="4d828-116">Windows пакет средств разработки программного обеспечения (SDK) (стандартный путь установки):% ProgramFiles% \\ пакеты sdk майкрософт \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ хтмледитриббон</span><span class="sxs-lookup"><span data-stu-id="4d828-116">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="4d828-117">Построение образца</span><span class="sxs-lookup"><span data-stu-id="4d828-117">Building the Sample</span></span>

<span data-ttu-id="4d828-118">Скачайте пример.</span><span class="sxs-lookup"><span data-stu-id="4d828-118">Download the sample.</span></span>

<span data-ttu-id="4d828-119">установите Windows SDK для Windows 7 и откройте командное окно среды сборки.</span><span class="sxs-lookup"><span data-stu-id="4d828-119">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="4d828-120">В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d828-120">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="4d828-121">Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца.</span><span class="sxs-lookup"><span data-stu-id="4d828-121">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="4d828-122">В командной строке введите команду MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="4d828-122">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="4d828-123">Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.</span><span class="sxs-lookup"><span data-stu-id="4d828-123">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="4d828-124">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="4d828-124">Running the Sample</span></span>

<span data-ttu-id="4d828-125">Чтобы запустить пример из окна командной строки среды сборки, выполните .exe файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.</span><span class="sxs-lookup"><span data-stu-id="4d828-125">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="4d828-126">Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="4d828-126">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="4d828-127">Поддержка</span><span class="sxs-lookup"><span data-stu-id="4d828-127">Support</span></span>

<span data-ttu-id="4d828-128">на [форуме Windows ribbon](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задать вопросы, связанные с разработкой приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="4d828-128">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="4d828-129">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="4d828-129">Minimum Requirements</span></span>



| <span data-ttu-id="4d828-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4d828-130">Requirement</span></span> | <span data-ttu-id="4d828-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4d828-131">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d828-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d828-132">Minimum supported client</span></span> | <span data-ttu-id="4d828-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d828-133">Windows 7</span></span><br/> <span data-ttu-id="4d828-134">Windows vista с пакетом обновления 2 (sp2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d828-134">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="4d828-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d828-135">Minimum supported server</span></span> | <span data-ttu-id="4d828-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d828-136">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="4d828-137">Windows сервер 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d828-137">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="4d828-138">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="4d828-138">Windows SDK</span></span>              | <span data-ttu-id="4d828-139">7.0</span><span class="sxs-lookup"><span data-stu-id="4d828-139">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="4d828-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4d828-140">Visual Studio</span></span>            | <span data-ttu-id="4d828-141">2008</span><span class="sxs-lookup"><span data-stu-id="4d828-141">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="4d828-142">Заголовочные и IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="4d828-142">Header and IDL files</span></span>     | <span data-ttu-id="4d828-143">уириббон. h, уириббон. idl</span><span class="sxs-lookup"><span data-stu-id="4d828-143">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="4d828-144">[обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows приложения ленты как Windows Vista, так и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4d828-144">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="4d828-145">обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="4d828-145">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="4d828-146">сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , Центр обновления Windows могут определить, установлено ли необходимое обновление. если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="4d828-146">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





