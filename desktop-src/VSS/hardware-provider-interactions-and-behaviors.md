---
description: Взаимодействие и поведение поставщика оборудования
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Взаимодействие и поведение поставщика оборудования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264026"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="9c466-103">Взаимодействие и поведение поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="9c466-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="9c466-104">Поставщики оборудования могут поддерживать теневые копии копирования при записи и (или) копирования зеркальных копий (разностных и (или) плексов).</span><span class="sxs-lookup"><span data-stu-id="9c466-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="9c466-105">Выделение ресурсов для теневых копий должно соответствовать контексту, указанному инициатором запроса в [**ивссбаккупкомпонентс:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), перечисленном в [**\_ \_ \_ контексте моментальных снимков VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), для набора теневых копий.</span><span class="sxs-lookup"><span data-stu-id="9c466-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="9c466-106">Если инициатор запроса указывает контекст теневой копии, поддерживаемый поставщиком, поставщик должен создать теневую копию с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="9c466-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="9c466-107">Если инициатор запроса указывает контекст теневой копии, который не поддерживается поставщиком, поставщик не должен пытаться создать теневую копию и вернуть **значение false** с помощью параметра *пбиссуппортед* в [**ивсшардвареснапшотпровидер:: арелунссуппортед**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span><span class="sxs-lookup"><span data-stu-id="9c466-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="9c466-108">Если в инициаторе запроса явно не указан контекст теневой копии, то поставщик должен использовать разумное поведение по умолчанию при создании теневой копии.</span><span class="sxs-lookup"><span data-stu-id="9c466-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="9c466-109">Поставщики оборудования, связанные с подсистемами RAID SAN, должны поддерживать перепереносимые теневые копии, чтобы разрешить перемещение между узлами в сети SAN.</span><span class="sxs-lookup"><span data-stu-id="9c466-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="9c466-110">Поставщики оборудования, запущенные на нескольких компьютерах в сети SAN, пока управляют одной и той же подсистемой RAID, не нуждаются в координации между поставщиками в сети хранения данных.</span><span class="sxs-lookup"><span data-stu-id="9c466-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="9c466-111">Координатор сохраняет все необходимое состояние.</span><span class="sxs-lookup"><span data-stu-id="9c466-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="9c466-112">Распознаются два вида состояний:</span><span class="sxs-lookup"><span data-stu-id="9c466-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="9c466-113">Состояние, необходимое для поддержки доступа к данным на томах, содержащихся в аппаратной теневой копии.</span><span class="sxs-lookup"><span data-stu-id="9c466-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="9c466-114">Сюда входит любое добавление тегов тома в режим «только для чтения» или «скрытый».</span><span class="sxs-lookup"><span data-stu-id="9c466-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="9c466-115">Это состояние должно быть на LUN оборудования и в поездках с LUN.</span><span class="sxs-lookup"><span data-stu-id="9c466-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="9c466-116">Это состояние сохраняется во всех эпохах загрузки и (или) обнаружении устройства.</span><span class="sxs-lookup"><span data-stu-id="9c466-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="9c466-117">Служба VSS управляет этим состоянием во время существования теневой копии.</span><span class="sxs-lookup"><span data-stu-id="9c466-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="9c466-118">Состояние, необходимое для распознавания определенного тома в составе набора теневых копий.</span><span class="sxs-lookup"><span data-stu-id="9c466-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="9c466-119">Это состояние сохраняется VSS в сочетании с инициатором запроса, который изначально создал набор теневых копий.</span><span class="sxs-lookup"><span data-stu-id="9c466-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="9c466-120">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="9c466-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9c466-121">Процесс создания теневой копии</span><span class="sxs-lookup"><span data-stu-id="9c466-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="9c466-122">Требуемые поведения для поставщиков теневого копирования</span><span class="sxs-lookup"><span data-stu-id="9c466-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="9c466-123">Переходы состояний в поставщиках теневого копирования</span><span class="sxs-lookup"><span data-stu-id="9c466-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="9c466-124">Обработка ошибок в поставщиках теневого копирования</span><span class="sxs-lookup"><span data-stu-id="9c466-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



