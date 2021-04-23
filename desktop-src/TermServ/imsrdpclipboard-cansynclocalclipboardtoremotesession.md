---
title: Метод IMsRdpClipboard CanSyncLocalClipboardToRemoteSession
description: Указывает, можно ли синхронизировать локальный буфер обмена с удаленным сеансом.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кансинклокалклипбоардторемотесессион
- Службы удаленных рабочих столов метода Кансинклокалклипбоардторемотесессион, интерфейс Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, метод Кансинклокалклипбоардторемотесессион
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719218"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="cbfc9-106">Метод Имсрдпклипбоард:: Кансинклокалклипбоардторемотесессион</span><span class="sxs-lookup"><span data-stu-id="cbfc9-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="cbfc9-107">Указывает, можно ли синхронизировать локальный буфер обмена с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="cbfc9-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfc9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbfc9-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="cbfc9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbfc9-109">Parameters</span></span>

<span data-ttu-id="cbfc9-110">**Значение true** , если локальный буфер обмена можно синхронизировать с удаленным сеансом; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="cbfc9-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbfc9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbfc9-111">Return value</span></span>

<span data-ttu-id="cbfc9-112">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="cbfc9-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfc9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cbfc9-113">Requirements</span></span>

| <span data-ttu-id="cbfc9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cbfc9-114">Requirement</span></span> | <span data-ttu-id="cbfc9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cbfc9-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="cbfc9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbfc9-116">Minimum supported client</span></span>| <span data-ttu-id="cbfc9-117">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="cbfc9-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="cbfc9-118">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cbfc9-118">Type library</span></span>            | <span data-ttu-id="cbfc9-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="cbfc9-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="cbfc9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cbfc9-120">DLL</span></span>                  | <span data-ttu-id="cbfc9-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="cbfc9-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="cbfc9-122">IID</span><span class="sxs-lookup"><span data-stu-id="cbfc9-122">IID</span></span>                      | <span data-ttu-id="cbfc9-123">IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="cbfc9-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="cbfc9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbfc9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfc9-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="cbfc9-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>