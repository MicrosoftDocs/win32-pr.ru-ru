---
description: API служба теневого копирования томов (VSS) предоставляет интерфейсы COM и C++ для поддержки создания инициаторов запросов и модулей записи.
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: Интерфейсы API теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1291f0e63b18530f92d99f9d526202df078fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145232"
---
# <a name="volume-shadow-copy-api-interfaces"></a><span data-ttu-id="3edf3-103">Интерфейсы API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="3edf3-103">Volume Shadow Copy API Interfaces</span></span>

<span data-ttu-id="3edf3-104">API служба теневого копирования томов (VSS) предоставляет интерфейсы COM и C++ для поддержки создания инициаторов запросов и модулей записи.</span><span class="sxs-lookup"><span data-stu-id="3edf3-104">The Volume Shadow Copy Service (VSS) API provides both COM and C++ interfaces to support the creation of requesters and writers.</span></span>

## <a name="vss-requester-specific-interfaces"></a><span data-ttu-id="3edf3-105">Интерфейсы Requester-Specific VSS</span><span class="sxs-lookup"><span data-stu-id="3edf3-105">VSS Requester-Specific Interfaces</span></span>

-   [<span data-ttu-id="3edf3-106">**ивссбаккупкомпонентс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-106">**IVssBackupComponents**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [<span data-ttu-id="3edf3-107">**ивссбаккупкомпонентсекс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-107">**IVssBackupComponentsEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [<span data-ttu-id="3edf3-108">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="3edf3-108">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [<span data-ttu-id="3edf3-109">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="3edf3-109">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [<span data-ttu-id="3edf3-110">**ивссексаминевритерметадата**</span><span class="sxs-lookup"><span data-stu-id="3edf3-110">**IVssExamineWriterMetadata**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [<span data-ttu-id="3edf3-111">**ивссексаминевритерметадатаекс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-111">**IVssExamineWriterMetadataEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [<span data-ttu-id="3edf3-112">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="3edf3-112">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [<span data-ttu-id="3edf3-113">**ивссвмкомпонент**</span><span class="sxs-lookup"><span data-stu-id="3edf3-113">**IVssWMComponent**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [<span data-ttu-id="3edf3-114">**ивссвритеркомпонентсекст**</span><span class="sxs-lookup"><span data-stu-id="3edf3-114">**IVssWriterComponentsExt**</span></span>](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a><span data-ttu-id="3edf3-115">Интерфейсы Writer-Specific VSS</span><span class="sxs-lookup"><span data-stu-id="3edf3-115">VSS Writer-Specific Interfaces</span></span>

-   [<span data-ttu-id="3edf3-116">**ивсскреатикспрессвритерметадата**</span><span class="sxs-lookup"><span data-stu-id="3edf3-116">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [<span data-ttu-id="3edf3-117">**ивсскреатевритерметадата**</span><span class="sxs-lookup"><span data-stu-id="3edf3-117">**IVssCreateWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [<span data-ttu-id="3edf3-118">**ивсскреатевритерметадатаекс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-118">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [<span data-ttu-id="3edf3-119">**ивссекспрессвритер**</span><span class="sxs-lookup"><span data-stu-id="3edf3-119">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [<span data-ttu-id="3edf3-120">**ивссвритеркомпонентс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-120">**IVssWriterComponents**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a><span data-ttu-id="3edf3-121">Интерфейсы Provider-Specific оборудования VSS</span><span class="sxs-lookup"><span data-stu-id="3edf3-121">VSS Hardware Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="3edf3-122">**ивссадмин**</span><span class="sxs-lookup"><span data-stu-id="3edf3-122">**IVssAdmin**</span></span>](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [<span data-ttu-id="3edf3-123">**ивсшардвареснапшотпровидер**</span><span class="sxs-lookup"><span data-stu-id="3edf3-123">**IVssHardwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [<span data-ttu-id="3edf3-124">**ивсшардвареснапшотпровидерекс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-124">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [<span data-ttu-id="3edf3-125">**ивсспровидеркреатеснапшотсет**</span><span class="sxs-lookup"><span data-stu-id="3edf3-125">**IVssProviderCreateSnapshotSet**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [<span data-ttu-id="3edf3-126">**ивсспровидернотификатионс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-126">**IVssProviderNotifications**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a><span data-ttu-id="3edf3-127">Интерфейсы Provider-Specific программного обеспечения VSS</span><span class="sxs-lookup"><span data-stu-id="3edf3-127">VSS Software Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="3edf3-128">**ивсссофтвареснапшотпровидер**</span><span class="sxs-lookup"><span data-stu-id="3edf3-128">**IVssSoftwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a><span data-ttu-id="3edf3-129">Общие интерфейсы VSS</span><span class="sxs-lookup"><span data-stu-id="3edf3-129">VSS Shared Interfaces</span></span>

-   [<span data-ttu-id="3edf3-130">**ивссасинк**</span><span class="sxs-lookup"><span data-stu-id="3edf3-130">**IVssAsync**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [<span data-ttu-id="3edf3-131">**ивсскомпонент**</span><span class="sxs-lookup"><span data-stu-id="3edf3-131">**IVssComponent**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [<span data-ttu-id="3edf3-132">**ивсскомпонентекс**</span><span class="sxs-lookup"><span data-stu-id="3edf3-132">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [<span data-ttu-id="3edf3-133">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="3edf3-133">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [<span data-ttu-id="3edf3-134">**ивссенумобжект**</span><span class="sxs-lookup"><span data-stu-id="3edf3-134">**IVssEnumObject**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [<span data-ttu-id="3edf3-135">**ивссвмдепенденци**</span><span class="sxs-lookup"><span data-stu-id="3edf3-135">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [<span data-ttu-id="3edf3-136">**ивссвмфиледеск**</span><span class="sxs-lookup"><span data-stu-id="3edf3-136">**IVssWMFiledesc**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a><span data-ttu-id="3edf3-137">Интерфейсы управления VSS</span><span class="sxs-lookup"><span data-stu-id="3edf3-137">VSS Management Interfaces</span></span>

-   [<span data-ttu-id="3edf3-138">**ивссдифферентиалсофтвареснапшотмгмт**</span><span class="sxs-lookup"><span data-stu-id="3edf3-138">**IVssDifferentialSoftwareSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [<span data-ttu-id="3edf3-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="3edf3-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [<span data-ttu-id="3edf3-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="3edf3-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [<span data-ttu-id="3edf3-141">**ивссенуммгмтобжект**</span><span class="sxs-lookup"><span data-stu-id="3edf3-141">**IVssEnumMgmtObject**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [<span data-ttu-id="3edf3-142">**ивссснапшотмгмт**</span><span class="sxs-lookup"><span data-stu-id="3edf3-142">**IVssSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [<span data-ttu-id="3edf3-143">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="3edf3-143">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
