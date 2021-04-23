---
title: Совместимость клиента и сервера — Windows 8
description: Совместимость клиента и сервера Windows 8 и Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "104335920"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="7c955-103">Совместимость клиента и сервера Windows 8 и Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c955-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="7c955-104">В этом разделе описаны изменения в операционной системе, о которых следует уделить особое внимание из-за возможных влияния на существующие приложения и о том, как новые приложения должны разрабатываться на клиентах, на серверах или на клиентах и серверах.</span><span class="sxs-lookup"><span data-stu-id="7c955-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="7c955-105">Ниже приведен список разделов, рассмотренных в этом разделе, сгруппированных по функциональным областям:</span><span class="sxs-lookup"><span data-stu-id="7c955-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="7c955-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="7c955-106">**AppCompat**</span></span>

-   <span data-ttu-id="7c955-107">Обновление правил обнаружения приложений безопасности</span><span class="sxs-lookup"><span data-stu-id="7c955-107">Security app detection rules update</span></span>
-   <span data-ttu-id="7c955-108">Определение состояния оболочки совместимости</span><span class="sxs-lookup"><span data-stu-id="7c955-108">Determining shim status</span></span>
-   <span data-ttu-id="7c955-109">Серверные приложения должны быть способны работать без графической оболочки сервера.</span><span class="sxs-lookup"><span data-stu-id="7c955-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="7c955-110">Компоненты сервера RDS удаляются из Windows 8</span><span class="sxs-lookup"><span data-stu-id="7c955-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="7c955-111">Модель сопоставления типов файлов и протоколов</span><span class="sxs-lookup"><span data-stu-id="7c955-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="7c955-112">Модератор активности на рабочем столе</span><span class="sxs-lookup"><span data-stu-id="7c955-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="7c955-113">Платформа .NET Framework 4,5 по умолчанию и платформа .NET Framework 3,5 являются необязательными</span><span class="sxs-lookup"><span data-stu-id="7c955-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="7c955-114">Классические приложения могут быть невидимыми после запуска веб-браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7c955-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="7c955-115">Режим высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="7c955-115">High-contrast mode</span></span>
-   <span data-ttu-id="7c955-116">Манифест приложения (исполняемый)</span><span class="sxs-lookup"><span data-stu-id="7c955-116">App (executable) manifest</span></span>
-   <span data-ttu-id="7c955-117">Текущая модель в очереди устарела</span><span class="sxs-lookup"><span data-stu-id="7c955-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="7c955-118">Сценарии помощника по совместимости программ для Windows 8</span><span class="sxs-lookup"><span data-stu-id="7c955-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="7c955-119">Мини-приложения рабочего стола удалены</span><span class="sxs-lookup"><span data-stu-id="7c955-119">Desktop gadgets removed</span></span>

<span data-ttu-id="7c955-120">**Хранилище и файловая система**</span><span class="sxs-lookup"><span data-stu-id="7c955-120">**Storage and File System**</span></span>

-   <span data-ttu-id="7c955-121">Обновление совместимости диска в расширенном формате (4 КБ)</span><span class="sxs-lookup"><span data-stu-id="7c955-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="7c955-122">Тонкая подготовка логических устройств</span><span class="sxs-lookup"><span data-stu-id="7c955-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="7c955-123">Расширенное хранилище теперь необязательно для среда предустановки Windows (WinPE) и SKU сервера.</span><span class="sxs-lookup"><span data-stu-id="7c955-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="7c955-124">Служба виртуальных дисков переходит на интерфейс API управления хранилищами Windows на основе инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7c955-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="7c955-125">Пользовательский интерфейс предыдущих версий удален для локальных томов</span><span class="sxs-lookup"><span data-stu-id="7c955-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="7c955-126">СторахЦи заменяет МСАХЦИ</span><span class="sxs-lookup"><span data-stu-id="7c955-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="7c955-127">Архивация и восстановление Windows 7 устарели</span><span class="sxs-lookup"><span data-stu-id="7c955-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="7c955-128">Разгрузка передачи данных</span><span class="sxs-lookup"><span data-stu-id="7c955-128">Offloaded data transfers</span></span>

<span data-ttu-id="7c955-129">**Другое**</span><span class="sxs-lookup"><span data-stu-id="7c955-129">**Other**</span></span>

-   <span data-ttu-id="7c955-130">диспетчер окон рабочего стола всегда включено</span><span class="sxs-lookup"><span data-stu-id="7c955-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="7c955-131">Direct2D не поддерживает отрисовку в "форматированные" метафайлы в Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="7c955-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="7c955-132">Изменения в поддержке устаревшего оборудования DX9</span><span class="sxs-lookup"><span data-stu-id="7c955-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="7c955-133">MSAA недоступен для приложений Магазина Windows</span><span class="sxs-lookup"><span data-stu-id="7c955-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="7c955-134">Порт 3 устарел для драйверов NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="7c955-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
