---
title: Интерфейс IMsRdpClipboard
description: Представляет контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, описание
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104139186"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="207b8-105">Интерфейс IMsRdpClipboard</span><span class="sxs-lookup"><span data-stu-id="207b8-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="207b8-106">Представляет контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена (то есть для свойства [мануалклипбоардсинценаблед](imsrdpextendedsettings-property.md) задано значение **true**).</span><span class="sxs-lookup"><span data-stu-id="207b8-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="207b8-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="207b8-107">Members</span></span>

<span data-ttu-id="207b8-108">Интерфейс **имсрдпклипбоард** наследует от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="207b8-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="207b8-109">**Имсрдпклипбоард** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="207b8-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="207b8-110">Методы</span><span class="sxs-lookup"><span data-stu-id="207b8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="207b8-111">Методы</span><span class="sxs-lookup"><span data-stu-id="207b8-111">Methods</span></span>

<span data-ttu-id="207b8-112">Интерфейс **имсрдпклипбоард** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="207b8-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="207b8-113">Метод</span><span class="sxs-lookup"><span data-stu-id="207b8-113">Method</span></span>        | <span data-ttu-id="207b8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="207b8-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="207b8-115">**кансинклокалклипбоардторемотесессион**</span><span class="sxs-lookup"><span data-stu-id="207b8-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="207b8-116">Указывает, можно ли синхронизировать локальный буфер обмена с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="207b8-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="207b8-117">**кансинкремотеклипбоардтолокалсессион**</span><span class="sxs-lookup"><span data-stu-id="207b8-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="207b8-118">Указывает, можно ли синхронизировать удаленный буфер обмена с локальным сеансом.</span><span class="sxs-lookup"><span data-stu-id="207b8-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="207b8-119">**синклокалклипбоардторемотесессион**</span><span class="sxs-lookup"><span data-stu-id="207b8-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="207b8-120">Синхронизирует локальный буфер обмена с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="207b8-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="207b8-121">**синкремотеклипбоардтолокалсессион**</span><span class="sxs-lookup"><span data-stu-id="207b8-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="207b8-122">Синхронизирует удаленный буфер обмена с локальным сеансом.</span><span class="sxs-lookup"><span data-stu-id="207b8-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="207b8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="207b8-123">Requirements</span></span>

| <span data-ttu-id="207b8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="207b8-124">Requirement</span></span> | <span data-ttu-id="207b8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="207b8-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="207b8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="207b8-126">Minimum supported client</span></span>| <span data-ttu-id="207b8-127">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="207b8-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="207b8-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="207b8-128">Type library</span></span>            | <span data-ttu-id="207b8-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="207b8-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="207b8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="207b8-130">DLL</span></span>                  | <span data-ttu-id="207b8-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="207b8-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="207b8-132">IID</span><span class="sxs-lookup"><span data-stu-id="207b8-132">IID</span></span>                      | <span data-ttu-id="207b8-133">IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="207b8-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="207b8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="207b8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207b8-135">**IMsRdpClientNonScriptable7:: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="207b8-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
