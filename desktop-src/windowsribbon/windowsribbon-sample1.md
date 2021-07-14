---
title: Пример Симплериббон
description: в этом примере кода демонстрируется реализация простого Windows приложения ленты.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: b2a7ab939239bd3c0017dfeeeab1487bcb1dce26
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691663"
---
# <a name="simpleribbon-sample"></a><span data-ttu-id="9668d-103">Пример Симплериббон</span><span class="sxs-lookup"><span data-stu-id="9668d-103">SimpleRibbon Sample</span></span>

<span data-ttu-id="9668d-104">в этом примере кода демонстрируется реализация простого Windows приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="9668d-104">This code sample demonstrates how to implement a simple Windows Ribbon application.</span></span>

- [<span data-ttu-id="9668d-105">Использование</span><span class="sxs-lookup"><span data-stu-id="9668d-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="9668d-106">Создание примера</span><span class="sxs-lookup"><span data-stu-id="9668d-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="9668d-107">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9668d-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="9668d-108">Поддержка</span><span class="sxs-lookup"><span data-stu-id="9668d-108">Support</span></span>](#support)
- [<span data-ttu-id="9668d-109">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="9668d-109">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="usage"></a><span data-ttu-id="9668d-110">Использование</span><span class="sxs-lookup"><span data-stu-id="9668d-110">Usage</span></span>

<span data-ttu-id="9668d-111">примеры платформы ленты Windows можно скачать в виде автономных Microsoft Visual Studio проектов из [центра загрузки майкрософт](https://www.microsoft.com/download/details.aspx?id=9620) или установить в составе [Windows пакета средств разработки программного обеспечения (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="9668d-111">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="9668d-112">Windows пакет средств разработки программного обеспечения (SDK) (стандартный путь установки):% ProgramFiles% \\ пакеты sdk майкрософт \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ симплериббон</span><span class="sxs-lookup"><span data-stu-id="9668d-112">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\SimpleRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="9668d-113">Построение образца</span><span class="sxs-lookup"><span data-stu-id="9668d-113">Building the Sample</span></span>

<span data-ttu-id="9668d-114">Скачайте пример.</span><span class="sxs-lookup"><span data-stu-id="9668d-114">Download the sample.</span></span>

<span data-ttu-id="9668d-115">установите Windows SDK для Windows 7 и откройте командное окно среды сборки.</span><span class="sxs-lookup"><span data-stu-id="9668d-115">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="9668d-116">В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.</span><span class="sxs-lookup"><span data-stu-id="9668d-116">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="9668d-117">Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца.</span><span class="sxs-lookup"><span data-stu-id="9668d-117">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="9668d-118">В командной строке введите команду MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="9668d-118">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="9668d-119">Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.</span><span class="sxs-lookup"><span data-stu-id="9668d-119">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="9668d-120">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9668d-120">Running the Sample</span></span>

<span data-ttu-id="9668d-121">Чтобы запустить пример из окна командной строки среды сборки, выполните .exe файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.</span><span class="sxs-lookup"><span data-stu-id="9668d-121">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="9668d-122">Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="9668d-122">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="9668d-123">Поддержка</span><span class="sxs-lookup"><span data-stu-id="9668d-123">Support</span></span>

<span data-ttu-id="9668d-124">на [форуме Windows ribbon](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задать вопросы, связанные с разработкой приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="9668d-124">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="9668d-125">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="9668d-125">Minimum Requirements</span></span>



| <span data-ttu-id="9668d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9668d-126">Requirement</span></span> | <span data-ttu-id="9668d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9668d-127">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9668d-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9668d-128">Minimum supported client</span></span> | <span data-ttu-id="9668d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9668d-129">Windows 7</span></span><br/> <span data-ttu-id="9668d-130">Windows vista с пакетом обновления 2 (sp2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="9668d-130">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="9668d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9668d-131">Minimum supported server</span></span> | <span data-ttu-id="9668d-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9668d-132">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="9668d-133">Windows сервер 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="9668d-133">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="9668d-134">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9668d-134">Windows SDK</span></span>              | <span data-ttu-id="9668d-135">7.0</span><span class="sxs-lookup"><span data-stu-id="9668d-135">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="9668d-136">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9668d-136">Visual Studio</span></span>            | <span data-ttu-id="9668d-137">2008</span><span class="sxs-lookup"><span data-stu-id="9668d-137">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="9668d-138">Заголовочные и IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="9668d-138">Header and IDL files</span></span>     | <span data-ttu-id="9668d-139">уириббон. h, уириббон. idl</span><span class="sxs-lookup"><span data-stu-id="9668d-139">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="9668d-140">[обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows приложения ленты как Windows Vista, так и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9668d-140">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="9668d-141">обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="9668d-141">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="9668d-142">сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , Центр обновления Windows могут определить, установлено ли необходимое обновление. если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9668d-142">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





