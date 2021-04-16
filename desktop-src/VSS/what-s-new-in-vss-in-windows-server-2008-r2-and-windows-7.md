---
description: В Windows Server 2008 R2 и Windows 7 внесены следующие изменения в служба теневого копирования томов.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Новые возможности: VSS в Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692345"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="35965-103">Новые возможности: VSS в Windows Server 2008 R2 & Windows 7</span><span class="sxs-lookup"><span data-stu-id="35965-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="35965-104">В Windows Server 2008 R2 и Windows 7 внесены следующие изменения в служба теневого копирования томов.</span><span class="sxs-lookup"><span data-stu-id="35965-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="35965-105">Новые интерфейсы VSS</span><span class="sxs-lookup"><span data-stu-id="35965-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="35965-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="35965-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="35965-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="35965-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="35965-108">**ивсскреатикспрессвритерметадата**</span><span class="sxs-lookup"><span data-stu-id="35965-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="35965-109">**ивссекспрессвритер**</span><span class="sxs-lookup"><span data-stu-id="35965-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="35965-110">Новые классы VSS</span><span class="sxs-lookup"><span data-stu-id="35965-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="35965-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="35965-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="35965-112">Новые перечисления VSS</span><span class="sxs-lookup"><span data-stu-id="35965-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="35965-113">**\_Параметры восстановления \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="35965-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="35965-114">Новые функции VSS</span><span class="sxs-lookup"><span data-stu-id="35965-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="35965-115">**креатевссекспрессвритер**</span><span class="sxs-lookup"><span data-stu-id="35965-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="35965-116">Существующие изменения интерфейса VSS</span><span class="sxs-lookup"><span data-stu-id="35965-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="35965-117">Интерфейс [**ивсшардвареснапшотпровидерекс**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)</span><span class="sxs-lookup"><span data-stu-id="35965-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="35965-118">Добавленный метод: [ **ресинклунс**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="35965-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="35965-119">Трассировка и ведение журнала событий VSS</span><span class="sxs-lookup"><span data-stu-id="35965-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="35965-120">Начиная с Windows Server 2008 R2 и Windows 7, для получения данных трассировки для инфраструктуры VSS можно использовать средство Всстраце, средство logman или средство tracelog.</span><span class="sxs-lookup"><span data-stu-id="35965-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="35965-121">Дополнительные сведения см. в разделе [использование средств трассировки с VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="35965-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="35965-122">Повторная синхронизация LUN</span><span class="sxs-lookup"><span data-stu-id="35965-122">LUN Resynchronization</span></span>

<span data-ttu-id="35965-123">В Windows Server 2008 R2 и Windows 7 инициаторы запросов VSS могут использовать функцию поставщика оборудования теневого копирования, называемую повторной синхронизацией LUN (или "синхронизация LUN").</span><span class="sxs-lookup"><span data-stu-id="35965-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="35965-124">Это схема быстрого восстановления, позволяющая администратору приложения восстанавливать данные из теневой копии на исходный логический номер устройства (LUN) или на новый LUN.</span><span class="sxs-lookup"><span data-stu-id="35965-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="35965-125">Теневая копия может быть полным клоном теневой копии или разностной теневой копией.</span><span class="sxs-lookup"><span data-stu-id="35965-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="35965-126">В любом случае, в конце операции повторной синхронизации, целевой LUN будет иметь то же содержимое, что и LUN теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="35965-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="35965-127">Во время операции повторной синхронизации массив выполняет копирование на уровне блока из теневой копии в целевой LUN.</span><span class="sxs-lookup"><span data-stu-id="35965-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="35965-128">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="35965-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="35965-129">Повторная синхронизация LUN — сценарий быстрого восстановления на сервере 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35965-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="35965-130">"Использование теневых копий в [Служба теневого копирования томов](/windows-server/storage/file-server/volume-shadow-copy-service)</span><span class="sxs-lookup"><span data-stu-id="35965-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="35965-131">Распространенные проблемы повторной синхронизации LUN</span><span class="sxs-lookup"><span data-stu-id="35965-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="35965-132">Модули записи Express</span><span class="sxs-lookup"><span data-stu-id="35965-132">Express Writers</span></span>

<span data-ttu-id="35965-133">В Windows Server 2008 R2 и Windows 7 интерфейс экспресс-выпуска VSS позволяет приложению регистрировать расположение файлов данных без реализации модуля записи VSS.</span><span class="sxs-lookup"><span data-stu-id="35965-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="35965-134">Дополнительные сведения см. в разделе [Служба теневого копирования томов (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span><span class="sxs-lookup"><span data-stu-id="35965-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="35965-135">Новые модули записи VSS</span><span class="sxs-lookup"><span data-stu-id="35965-135">New VSS Writers</span></span>

<span data-ttu-id="35965-136">В Windows Server 2008 R2 и Windows 7 представлены следующие модули записи VSS:</span><span class="sxs-lookup"><span data-stu-id="35965-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="35965-137">Модуль записи счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="35965-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="35965-138">Модуль записи планировщик задач</span><span class="sxs-lookup"><span data-stu-id="35965-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="35965-139">Модуль записи хранилища метаданных VSS</span><span class="sxs-lookup"><span data-stu-id="35965-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="35965-140">Эти новые модули записи описаны в встроенных [модулях записи VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="35965-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
