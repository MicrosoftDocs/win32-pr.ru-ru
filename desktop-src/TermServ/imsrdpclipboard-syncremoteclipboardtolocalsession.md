---
title: Метод IMsRdpClipboard SyncRemoteClipboardToLocalSession
description: Синхронизирует удаленный буфер обмена с локальным сеансом.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Синкремотеклипбоардтолокалсессион
- Службы удаленных рабочих столов метода Синкремотеклипбоардтолокалсессион, интерфейс Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, метод Синкремотеклипбоардтолокалсессион
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d397d7c1ca4407a5125877721be9aa022f8132a7
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536395"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="74dd6-106">Метод Имсрдпклипбоард:: Синкремотеклипбоардтолокалсессион</span><span class="sxs-lookup"><span data-stu-id="74dd6-106">IMsRdpClipboard::SyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="74dd6-107">Синхронизирует удаленный буфер обмена с локальным сеансом.</span><span class="sxs-lookup"><span data-stu-id="74dd6-107">Syncs the remote Clipboard to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="74dd6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74dd6-108">Syntax</span></span>

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a><span data-ttu-id="74dd6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="74dd6-109">Parameters</span></span>

<span data-ttu-id="74dd6-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="74dd6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74dd6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74dd6-111">Return value</span></span>

<span data-ttu-id="74dd6-112">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="74dd6-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="74dd6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="74dd6-113">Requirements</span></span>

| <span data-ttu-id="74dd6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="74dd6-114">Requirement</span></span> | <span data-ttu-id="74dd6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="74dd6-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="74dd6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74dd6-116">Minimum supported client</span></span>| <span data-ttu-id="74dd6-117">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="74dd6-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="74dd6-118">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="74dd6-118">Type library</span></span>            | <span data-ttu-id="74dd6-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="74dd6-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="74dd6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="74dd6-120">DLL</span></span>                  | <span data-ttu-id="74dd6-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="74dd6-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="74dd6-122">IID</span><span class="sxs-lookup"><span data-stu-id="74dd6-122">IID</span></span>                      | <span data-ttu-id="74dd6-123">IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="74dd6-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="74dd6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74dd6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74dd6-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="74dd6-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>