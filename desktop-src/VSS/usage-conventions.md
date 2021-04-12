---
description: При разработке собственного приложения VSS следует учитывать следующие рекомендации и ограничения.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Совместимость приложений VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343582"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="ddb49-103">Совместимость приложений VSS</span><span class="sxs-lookup"><span data-stu-id="ddb49-103">VSS Application Compatibility</span></span>

<span data-ttu-id="ddb49-104">При разработке собственного приложения VSS следует учитывать следующие рекомендации и ограничения.</span><span class="sxs-lookup"><span data-stu-id="ddb49-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="ddb49-105">Может оказаться полезным ознакомиться с примером кода для инициаторов запросов VSS, поставщиков и модулей записи, предоставляемых пакетом SDK для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ddb49-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="ddb49-106">Windows SDK можно использовать для разработки приложений VSS только для Windows Vista и более поздних версий операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ddb49-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="ddb49-107">Его нельзя использовать для разработки запросов VSS, поставщиков или модулей записи для Windows Server 2003 R2, Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ddb49-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="ddb49-108">**Windows server 2003 R2, Windows server 2003 и Windows XP:** Служба VSS доступна в пакете SDK для служба теневого копирования томов 7,2, который можно скачать из [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) .</span><span class="sxs-lookup"><span data-stu-id="ddb49-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="ddb49-109">Обратите внимание, что \\ для 64-разрядных версий Windows server 2003 R2, Windows server 2003 и Windows XP можно использовать 64-битные файлы вссапи. lib в каталогах, которые находятся в каталоге файлов Win2003.</span><span class="sxs-lookup"><span data-stu-id="ddb49-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="ddb49-110">Этот пакет SDK также содержит образцы кода для инициаторов запросов VSS, поставщиков и модулей записи.</span><span class="sxs-lookup"><span data-stu-id="ddb49-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="ddb49-111">Компиляция приложений VSS</span><span class="sxs-lookup"><span data-stu-id="ddb49-111">Compiling VSS Applications</span></span>

<span data-ttu-id="ddb49-112">При разработке инициатора запроса, например приложения резервного копирования:</span><span class="sxs-lookup"><span data-stu-id="ddb49-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="ddb49-113">Включите следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="ddb49-113">Include the following headers:</span></span> <dl> <span data-ttu-id="ddb49-114">VSS. h</span><span class="sxs-lookup"><span data-stu-id="ddb49-114">Vss.h</span></span>  
    <span data-ttu-id="ddb49-115">Всвритер. h</span><span class="sxs-lookup"><span data-stu-id="ddb49-115">VsWriter.h</span></span>  
    <span data-ttu-id="ddb49-116">Всбаккуп. h</span><span class="sxs-lookup"><span data-stu-id="ddb49-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="ddb49-117">Вссапи. lib</span><span class="sxs-lookup"><span data-stu-id="ddb49-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="ddb49-118">При разработке модуля записи:</span><span class="sxs-lookup"><span data-stu-id="ddb49-118">When developing a writer:</span></span>

-   <span data-ttu-id="ddb49-119">Включите следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="ddb49-119">Include the following headers:</span></span> <dl> <span data-ttu-id="ddb49-120">VSS. h</span><span class="sxs-lookup"><span data-stu-id="ddb49-120">Vss.h</span></span>  
    <span data-ttu-id="ddb49-121">Всвритер. h</span><span class="sxs-lookup"><span data-stu-id="ddb49-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="ddb49-122">Вссапи. lib</span><span class="sxs-lookup"><span data-stu-id="ddb49-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="ddb49-123">Поддерживаемые конфигурации и ограничения</span><span class="sxs-lookup"><span data-stu-id="ddb49-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="ddb49-124">В следующем списке перечислены поддерживаемые конфигурации и ограничения.</span><span class="sxs-lookup"><span data-stu-id="ddb49-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="ddb49-125">Служба VSS предоставляется и поддерживается в версиях операционной системы Windows, начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ddb49-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="ddb49-126">В следующей таблице приведены сведения о совместимости между версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="ddb49-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="ddb49-127">Обратите внимание, что если приложение VSS "скомпилировано для" указанной версии Windows, это означает, что приложение было скомпилировано с использованием файлов заголовков и библиотек, относящихся к этой версии.</span><span class="sxs-lookup"><span data-stu-id="ddb49-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="ddb49-128">Поставщики оборудования будут работать только в версиях операционных систем Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ddb49-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="ddb49-129">Они не будут работать в версиях клиентских операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="ddb49-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="ddb49-130">В следующих таблицах Windows Server 2008 с пакетом обновления 2 (SP2) должен рассматриваться как Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ddb49-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="ddb49-131">Дополнительные сведения о Windows Server 2008 с пакетом обновления 2 (SP2) см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=178730> .</span><span class="sxs-lookup"><span data-stu-id="ddb49-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="ddb49-132">Windows Server 2003 R2 следует рассматривать как Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ddb49-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="ddb49-133">Если приложение VSS скомпилировано для Windows Server 2003 или более поздней версии, оно также будет работать в более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="ddb49-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="ddb49-134">Инициаторы запросов, модули записи и поставщики VSS, скомпилированные для</span><span class="sxs-lookup"><span data-stu-id="ddb49-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="ddb49-135">Будет выполняться на</span><span class="sxs-lookup"><span data-stu-id="ddb49-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="ddb49-136">Windows Server 2008 R2 (64-разрядная версия), Windows 7 (64-bit), Windows Server 2008 (64-bit) и Windows Vista (64-bit)</span><span class="sxs-lookup"><span data-stu-id="ddb49-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="ddb49-137">Windows Server 2008 R2 (64-разрядная версия), Windows 7 (64-bit), Windows Server 2008 (64-bit) и Windows Vista (64-bit)</span><span class="sxs-lookup"><span data-stu-id="ddb49-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ddb49-138">Windows Server 2008 R2 (32-разрядная версия), Windows 7 (32-bit), Windows Server 2008 (32-bit) и Windows Vista (32-bit)</span><span class="sxs-lookup"><span data-stu-id="ddb49-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="ddb49-139">Windows Server 2008 R2 (32-разрядная версия), Windows 7 (32-bit), Windows Server 2008 (32-bit) и Windows Vista (32-bit)</span><span class="sxs-lookup"><span data-stu-id="ddb49-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="ddb49-140">Windows Server 2003 (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="ddb49-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="ddb49-141">Windows Server 2008 R2 (64-разрядная версия), Windows 7 (64-bit), Windows Server 2008 (64-разрядная), Windows Vista (64-bit) и Windows Server 2003 (64-bit)</span><span class="sxs-lookup"><span data-stu-id="ddb49-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ddb49-142">Windows Server 2003 (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="ddb49-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="ddb49-143">Windows Server 2008 R2 (32-разрядная версия), Windows 7 (32-bit), Windows Server 2008 (32-разрядная), Windows Vista (32-bit) и Windows Server 2003 (32-bit)</span><span class="sxs-lookup"><span data-stu-id="ddb49-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="ddb49-144">Инициаторы запроса также будут работать на Windows Server 2003 (64-bit).</span><span class="sxs-lookup"><span data-stu-id="ddb49-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="ddb49-145">Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="ddb49-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="ddb49-146">Windows Server 2003 (64-bit) и Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="ddb49-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ddb49-147">Windows XP (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="ddb49-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="ddb49-148">Windows XP (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="ddb49-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="ddb49-149">Компиляция инициатора запроса, модуля записи или поставщика VSS для</span><span class="sxs-lookup"><span data-stu-id="ddb49-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="ddb49-150">Использовать</span><span class="sxs-lookup"><span data-stu-id="ddb49-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ddb49-151">Windows Server 2008 R2 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="ddb49-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="ddb49-152">Windows SDK для Windows 7 (доступно в [центре загрузки Windows](https://www.microsoft.com/download/details.aspx?id=8279)).</span><span class="sxs-lookup"><span data-stu-id="ddb49-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="ddb49-153">Windows Server 2008 или Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddb49-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="ddb49-154">Windows SDK для Windows Server 2008 (доступно в [центре разработчиков Windows SDK](https://msdn.microsoft.com/windows/bb980924.aspx)).</span><span class="sxs-lookup"><span data-stu-id="ddb49-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="ddb49-155">Windows Server 2003 R2, Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ddb49-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="ddb49-156">Пакет SDK для служба теневого копирования томов 7,2</span><span class="sxs-lookup"><span data-stu-id="ddb49-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="ddb49-157">Все 32-разрядные приложения VSS (инициаторы запросов, поставщики и модули записи) должны выполняться как собственные 32-разрядные или 64-разрядные приложения.</span><span class="sxs-lookup"><span data-stu-id="ddb49-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="ddb49-158">Их запуск в эмуляторе WOW64 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ddb49-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="ddb49-159">**Windows Server 2003 и Windows XP:** Запуск 32-разрядов запросов VSS в эмуляторе WOW64 поддерживается, но не для резервных копий состояния системы.</span><span class="sxs-lookup"><span data-stu-id="ddb49-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="ddb49-160">Запуск 32-разрядных поставщиков VSS и модулей записи в эмуляторе WOW64 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ddb49-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="ddb49-161">Поддержка запуска 32-разрядных запросов в подсистеме WOW64 была удалена в Windows Vista и последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="ddb49-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="ddb49-162">Теневую копию, созданную в Windows Server 2003 R2 или Windows Server 2003, нельзя использовать на компьютере под Windows Server 2008 R2 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ddb49-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="ddb49-163">Теневую копию, созданную в Windows Server 2008 R2 или Windows Server 2008, нельзя использовать на компьютере под Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ddb49-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="ddb49-164">Однако теневую копию, созданную в Windows Server 2008, можно использовать на компьютере, работающем под Windows Server 2008 R2, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="ddb49-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="ddb49-165">Для поддержки теневых копий система, в которой работает VSS, должна иметь по крайней мере одну файловую систему NTFS.</span><span class="sxs-lookup"><span data-stu-id="ddb49-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="ddb49-166">В этой файловой системе будет размещена область инструмента для копирования теневой копии.</span><span class="sxs-lookup"><span data-stu-id="ddb49-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="ddb49-167">Дополнительные сведения см. в разделе [поставщик системы](providers.md).</span><span class="sxs-lookup"><span data-stu-id="ddb49-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="ddb49-168">С учетом наличия одной файловой системы NTFS и выбора соответствующего контекста (см. раздел [конфигурации контекста теневого копирования](shadow-copy-context-configurations.md)) любая поддерживаемая локальная файловая система может быть теневой.</span><span class="sxs-lookup"><span data-stu-id="ddb49-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="ddb49-169">Теневые копии можно создавать только для локально подключенных файловых систем.</span><span class="sxs-lookup"><span data-stu-id="ddb49-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="ddb49-170">Удаленные общие папки и другие перекрестные файловые системы не могут быть скопированы системой, в которой они будут подключены.</span><span class="sxs-lookup"><span data-stu-id="ddb49-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="ddb49-171">Эти файловые системы могут быть теневыми копиями только системами, которые обслуживают файловые системы.</span><span class="sxs-lookup"><span data-stu-id="ddb49-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="ddb49-172">Модули записи и инициаторы должны указывать только локальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ddb49-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="ddb49-173">Локальные ресурсы — это наборы файлов, абсолютный путь к которым начинается с буквы диска, а буква диска не может быть связана с подключенной папкой в удаленной общей папке.</span><span class="sxs-lookup"><span data-stu-id="ddb49-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="ddb49-174">Максимальное число теневых копий программного обеспечения для каждого тома — 512.</span><span class="sxs-lookup"><span data-stu-id="ddb49-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="ddb49-175">Однако по умолчанию вы можете поддерживать 64 теневых копий, используемых теневыми копиями компонента "Общие папки".</span><span class="sxs-lookup"><span data-stu-id="ddb49-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="ddb49-176">Чтобы изменить ограничение для теневых копий компонента "Общие папки", используйте раздел реестра [максшадовкопиес](../backup/registry-keys-for-backup-and-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb49-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="ddb49-177">Инфраструктура компонентов резервного копирования не поддерживает резервное копирование ресурсов кластера в качестве компонентов модуля записи.</span><span class="sxs-lookup"><span data-stu-id="ddb49-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="ddb49-178">Для резервного копирования ресурсов кластера приложения должны предположить, что путь является локальным для указанного узла кластера.</span><span class="sxs-lookup"><span data-stu-id="ddb49-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="ddb49-179">Корпорация Майкрософт не предоставляет техническую поддержку для разработчиков и ИТ-специалистов по внедрению оперативного восстановления состояния системы в Windows (все выпуски).</span><span class="sxs-lookup"><span data-stu-id="ddb49-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="ddb49-180">При резервном копировании и восстановлении состояния системы рекомендуемой стратегией является резервное копирование и восстановление системных и загрузочных томов в дополнение к файлам, перечисленным модулями записи состояния системы.</span><span class="sxs-lookup"><span data-stu-id="ddb49-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="ddb49-181">Модули записи состояния системы — это модули записи, для которых в качестве атрибута [**\_ \_ типа использования VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) задано значение VSS \_ UT \_ бутаблесистемстате или VSS \_ UT \_ системсервице.</span><span class="sxs-lookup"><span data-stu-id="ddb49-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
