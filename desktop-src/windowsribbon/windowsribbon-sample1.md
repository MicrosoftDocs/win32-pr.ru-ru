---
title: Пример Симплериббон
description: В этом примере кода показано, как реализовать простое приложение ленты Windows.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5055d47db2d947778699d55bbae96649b9b45ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492495"
---
# <a name="simpleribbon-sample"></a><span data-ttu-id="9ee7e-103">Пример Симплериббон</span><span class="sxs-lookup"><span data-stu-id="9ee7e-103">SimpleRibbon Sample</span></span>

<span data-ttu-id="9ee7e-104">В этом примере кода показано, как реализовать простое приложение ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-104">This code sample demonstrates how to implement a simple Windows Ribbon application.</span></span>

-   [<span data-ttu-id="9ee7e-105">Использование</span><span class="sxs-lookup"><span data-stu-id="9ee7e-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="9ee7e-106">Создание примера</span><span class="sxs-lookup"><span data-stu-id="9ee7e-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="9ee7e-107">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9ee7e-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="9ee7e-108">Поддержка</span><span class="sxs-lookup"><span data-stu-id="9ee7e-108">Support</span></span>](#support)
-   [<span data-ttu-id="9ee7e-109">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="9ee7e-109">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="usage"></a><span data-ttu-id="9ee7e-110">Использование</span><span class="sxs-lookup"><span data-stu-id="9ee7e-110">Usage</span></span>

<span data-ttu-id="9ee7e-111">Пример Симплериббон можно скачать как автономный проект Microsoft Visual Studio из [центра загрузки Майкрософт](https://www.microsoft.com/DOWNLOADS/en/default.aspx) или установить в составе [пакета средств разработки программного обеспечения (SDK) для Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ee7e-111">The SimpleRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="9ee7e-112">Центр загрузки Майкрософт: [примеры для ленты Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="9ee7e-112">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="9ee7e-113">Пакет средств разработки программного обеспечения (SDK) для Windows (стандартный путь установки):% ProgramFiles% \\ пакеты SDK Microsoft \\ Windows \\ \[ номер версии \] \\ примеры \\ винуи \\ виндовсриббон \\ симплериббон</span><span class="sxs-lookup"><span data-stu-id="9ee7e-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\SimpleRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="9ee7e-114">Построение образца</span><span class="sxs-lookup"><span data-stu-id="9ee7e-114">Building the Sample</span></span>

<span data-ttu-id="9ee7e-115">Загрузите пример на жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-115">Download the sample to your hard disk.</span></span>

<span data-ttu-id="9ee7e-116">Установите Windows SDK для Windows 7 и Откройте командное окно среды сборки.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="9ee7e-117">В меню &quot;Пуск&quot; выделите пункты &quot;Все программы&quot;, &quot;Пакет SDK для Microsoft Windows&quot;, а затем &quot;Оболочки CMD&quot;.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="9ee7e-118">Чтобы построить образец из окна командной строки среды построения, перейдите в исходный каталог образца.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="9ee7e-119">В командной строке введите команду MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="9ee7e-120">Чтобы построить образец в Microsoft Visual Studio, загрузите решение образца или файл проекта и нажмите сочетание клавиш CTRL + SHIFT + B.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="9ee7e-121">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9ee7e-121">Running the Sample</span></span>

<span data-ttu-id="9ee7e-122">Чтобы запустить пример из командного окна среды сборки, выполните EXE файлы в \\ папке bin Debug или Bin release, которая \\ содержится в исходной папке Sample.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="9ee7e-123">Для запуска скомпилированного образца с помощью отладки в Visual Studio, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="9ee7e-124">Поддержка</span><span class="sxs-lookup"><span data-stu-id="9ee7e-124">Support</span></span>

<span data-ttu-id="9ee7e-125">На [форуме по разработке ленты Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) можно обсудить темы и задавать вопросы, связанные с разработкой приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="9ee7e-126">Минимальные требования</span><span class="sxs-lookup"><span data-stu-id="9ee7e-126">Minimum Requirements</span></span>



| <span data-ttu-id="9ee7e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9ee7e-127">Requirement</span></span> | <span data-ttu-id="9ee7e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9ee7e-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee7e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ee7e-129">Minimum supported client</span></span> | <span data-ttu-id="9ee7e-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ee7e-130">Windows 7</span></span><br/> <span data-ttu-id="9ee7e-131">Windows Vista с пакетом обновления 2 (SP2) и [обновлением платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ee7e-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="9ee7e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ee7e-132">Minimum supported server</span></span> | <span data-ttu-id="9ee7e-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ee7e-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="9ee7e-134">Windows Server 2008 с пакетом обновления 2 (SP2) и [обновлением платформы для Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ee7e-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="9ee7e-135">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9ee7e-135">Windows SDK</span></span>              | <span data-ttu-id="9ee7e-136">7.0</span><span class="sxs-lookup"><span data-stu-id="9ee7e-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="9ee7e-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9ee7e-137">Visual Studio</span></span>            | <span data-ttu-id="9ee7e-138">2008</span><span class="sxs-lookup"><span data-stu-id="9ee7e-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="9ee7e-139">Заголовочные и IDL-файлы</span><span class="sxs-lookup"><span data-stu-id="9ee7e-139">Header and IDL files</span></span>     | <span data-ttu-id="9ee7e-140">уириббон. h, уириббон. idl</span><span class="sxs-lookup"><span data-stu-id="9ee7e-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="9ee7e-141">[Обновление платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) и [обновление платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) — это наборы библиотек времени выполнения, которые позволяют разработчикам ориентироваться на Windows vista и Windows Server 2008 для приложений ленты Windows.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="9ee7e-142">Обновления платформы будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="9ee7e-143">Сторонние приложения, требующие [обновления платформы для Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) или [обновления платформы для Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) , могут иметь центр обновления Windows определить, установлена ли требуемая обновленная система. Если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9ee7e-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





