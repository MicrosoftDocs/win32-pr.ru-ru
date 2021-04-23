---
title: Метод IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Указывает, можно ли синхронизировать удаленный буфер обмена с локальным сеансом.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кансинкремотеклипбоардтолокалсессион
- Службы удаленных рабочих столов метода Кансинкремотеклипбоардтолокалсессион, интерфейс Имсрдпклипбоард
- Службы удаленных рабочих столов интерфейса Имсрдпклипбоард, метод Кансинкремотеклипбоардтолокалсессион
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719231"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="b2619-106">Метод Имсрдпклипбоард:: Кансинкремотеклипбоардтолокалсессион</span><span class="sxs-lookup"><span data-stu-id="b2619-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="b2619-107">Указывает, можно ли синхронизировать удаленный буфер обмена с локальным сеансом.</span><span class="sxs-lookup"><span data-stu-id="b2619-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2619-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2619-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="b2619-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2619-109">Parameters</span></span>

<span data-ttu-id="b2619-110">**Значение true** , если удаленный буфер обмена можно синхронизировать с локальным сеансом; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b2619-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2619-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2619-111">Return value</span></span>

<span data-ttu-id="b2619-112">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="b2619-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2619-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b2619-113">Requirements</span></span>

| <span data-ttu-id="b2619-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b2619-114">Requirement</span></span> | <span data-ttu-id="b2619-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b2619-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="b2619-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2619-116">Minimum supported client</span></span>| <span data-ttu-id="b2619-117">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="b2619-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="b2619-118">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b2619-118">Type library</span></span>            | <span data-ttu-id="b2619-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b2619-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="b2619-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b2619-120">DLL</span></span>                  | <span data-ttu-id="b2619-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b2619-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="b2619-122">IID</span><span class="sxs-lookup"><span data-stu-id="b2619-122">IID</span></span>                      | <span data-ttu-id="b2619-123">IID \_ имсрдпклипбоард определен как 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="b2619-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="b2619-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2619-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2619-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="b2619-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>