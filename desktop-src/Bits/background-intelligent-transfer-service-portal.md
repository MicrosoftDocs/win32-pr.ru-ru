---
title: Фоновая интеллектуальная служба передачи
description: Фоновая интеллектуальная служба передачи данных (BITS) передает (загружает или отправляет) данные между клиентом и сервером, а также отображает данные о ходе выполнения передачи.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Фоновая интеллектуальная служба передачи
- Фоновая интеллектуальная служба передачи, начальная страница
- BITS (см. фоновая интеллектуальная служба передачи)
- скачивание битов файлов
- фоновые биты передачи файлов
- отправка битов файлов
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987757"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="39cfb-109">Фоновая интеллектуальная служба передачи</span><span class="sxs-lookup"><span data-stu-id="39cfb-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="39cfb-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="39cfb-110">Purpose</span></span>

<span data-ttu-id="39cfb-111">Фоновая интеллектуальная служба передачи (BITS) используется программистами и системными администраторами для загрузки файлов или передачи файлов на веб-серверы HTTP и файловые ресурсы SMB.</span><span class="sxs-lookup"><span data-stu-id="39cfb-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="39cfb-112">Служба BITS будет принимать затраты на пересылку, а также использовать сеть, чтобы обеспечить минимально возможное влияние на рабочую нагрузку пользователя.</span><span class="sxs-lookup"><span data-stu-id="39cfb-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="39cfb-113">Службы BITS также обрабатывают интеруптионс сети, приостанавливая и автоматически возобновляя передачу, даже после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="39cfb-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="39cfb-114">Службы BITS включают командлеты PowerShell для создания и управления передачами, а также служебную программу командной строки Битсадмин.</span><span class="sxs-lookup"><span data-stu-id="39cfb-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="39cfb-115">Служба BITS может использоваться Windows для загрузки обновлений в локальную систему.</span><span class="sxs-lookup"><span data-stu-id="39cfb-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="39cfb-116">Если вы являетесь конечным пользователем для поиска способов устранения неполадок установки BITS, см. статью [Устранение проблем Центр обновления Windows](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span><span class="sxs-lookup"><span data-stu-id="39cfb-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="39cfb-117">Где применимо</span><span class="sxs-lookup"><span data-stu-id="39cfb-117">Where applicable</span></span>

<span data-ttu-id="39cfb-118">Используйте службы BITS для приложений, которые должны:</span><span class="sxs-lookup"><span data-stu-id="39cfb-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="39cfb-119">Скачайте файлы или отправьте их на веб-сервер HTTP или в Интернет или на файловый сервер SMB.</span><span class="sxs-lookup"><span data-stu-id="39cfb-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="39cfb-120">Автоматическое возобновление передачи файлов после отключения сети и перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="39cfb-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="39cfb-121">Сохранение скорости реагирования других сетевых приложений.</span><span class="sxs-lookup"><span data-stu-id="39cfb-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="39cfb-122">Будьте учитывать по стоимости сети (например, роуминговые сети).</span><span class="sxs-lookup"><span data-stu-id="39cfb-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="39cfb-123">При необходимости можно работать с [BranchCache](/windows-server/networking/branchcache/branchcache) для оптимизации трафика глобальной сети (WAN).</span><span class="sxs-lookup"><span data-stu-id="39cfb-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="39cfb-124">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="39cfb-124">Developer audience</span></span>

<span data-ttu-id="39cfb-125">Служба BITS — это COM-интерфейс, предназначенный для разработчиков на C и C++, который также может использоваться разработчиками .NET.</span><span class="sxs-lookup"><span data-stu-id="39cfb-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="39cfb-126">Разработчики UWP должны использовать API [Windows. Networking. баккграундтрансфер](/uwp/api/Windows.Networking.BackgroundTransfer) , а не API BITS.</span><span class="sxs-lookup"><span data-stu-id="39cfb-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="39cfb-127">Версии BITS</span><span class="sxs-lookup"><span data-stu-id="39cfb-127">BITS versions</span></span>

<span data-ttu-id="39cfb-128">Полный журнал версий и сведения о более ранней версии операционной системы см. в разделе [новые](what-s-new.md)возможности.</span><span class="sxs-lookup"><span data-stu-id="39cfb-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="39cfb-129">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="39cfb-129">In this section</span></span>



| <span data-ttu-id="39cfb-130">Раздел</span><span class="sxs-lookup"><span data-stu-id="39cfb-130">Topic</span></span>                                                           | <span data-ttu-id="39cfb-131">Описание</span><span class="sxs-lookup"><span data-stu-id="39cfb-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39cfb-132">Сведения о службе BITS</span><span class="sxs-lookup"><span data-stu-id="39cfb-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="39cfb-133">Общие сведения о службе BITS.</span><span class="sxs-lookup"><span data-stu-id="39cfb-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="39cfb-134">Использование BITS</span><span class="sxs-lookup"><span data-stu-id="39cfb-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="39cfb-135">Процедурное пошаговое описание разработки клиентов BITS, которые передают файлы между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="39cfb-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="39cfb-136">Справочник по BITS</span><span class="sxs-lookup"><span data-stu-id="39cfb-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="39cfb-137">Справочные сведения по интерфейсам программирования BITS.</span><span class="sxs-lookup"><span data-stu-id="39cfb-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="39cfb-138">Также содержит сведения о примерах, средствах, параметрах сервера для отправки заданий и протоколе передачи.</span><span class="sxs-lookup"><span data-stu-id="39cfb-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="39cfb-139">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="39cfb-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="39cfb-140">Сведения, которые следует учитывать при проектировании приложения, использующего BITS.</span><span class="sxs-lookup"><span data-stu-id="39cfb-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="39cfb-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="39cfb-141">Additional resources</span></span>

<span data-ttu-id="39cfb-142">Ниже приведены дополнительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="39cfb-142">The following are additional resources.</span></span>


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39cfb-143">DLL-библиотека ссылок .NET</span><span class="sxs-lookup"><span data-stu-id="39cfb-143">.NET Reference DLL</span></span>   | <span data-ttu-id="39cfb-144">Сведения об использовании BITS из .NET с помощью справочника DLL см. в разделе [вызов в BITS из .NET с помощью справочника DLL](/windows/desktop/Bits/bits-dot-net) .</span><span class="sxs-lookup"><span data-stu-id="39cfb-144">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="39cfb-145">Оболочка .NET</span><span class="sxs-lookup"><span data-stu-id="39cfb-145">.NET Wrapper</span></span>   | <span data-ttu-id="39cfb-146">Для других оболочек .NET для BITS можно выполнить поиск по [NuGet](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) для проектов, помеченных тегом BITS.</span><span class="sxs-lookup"><span data-stu-id="39cfb-146">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

