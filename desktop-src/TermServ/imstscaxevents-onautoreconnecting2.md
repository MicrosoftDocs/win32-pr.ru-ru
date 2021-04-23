---
title: Имстскаксевентс OnAutoReconnecting2, метод
description: Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов). | Имстскаксевентс OnAutoReconnecting2, метод
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnAutoReconnecting2
- Службы удаленных рабочих столов метода OnAutoReconnecting2, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684930"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="923fe-107">Метод Имстскаксевентс:: OnAutoReconnecting2</span><span class="sxs-lookup"><span data-stu-id="923fe-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="923fe-108">Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="923fe-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="923fe-109">Это улучшенная версия метода [**онаутореконнектинг**](-imstscaxevents--onautoreconnecting.md) .</span><span class="sxs-lookup"><span data-stu-id="923fe-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="923fe-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="923fe-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="923fe-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="923fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="923fe-112">*дисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="923fe-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="923fe-113">Код, описывающий причину последнего отключения сеанса.</span><span class="sxs-lookup"><span data-stu-id="923fe-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="923fe-114">*нетворкаваилабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="923fe-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="923fe-115">Указывает, доступна ли сеть.</span><span class="sxs-lookup"><span data-stu-id="923fe-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="923fe-116">*аттемпткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="923fe-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="923fe-117">Число попыток, выполненных в текущем процессе автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="923fe-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="923fe-118">Это число увеличивается на единицу при каждой попытке.</span><span class="sxs-lookup"><span data-stu-id="923fe-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="923fe-119">*максаттемпткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="923fe-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="923fe-120">Максимальное число попыток, которое будет выполнено в текущем процессе автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="923fe-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="923fe-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="923fe-121">Return value</span></span>

<span data-ttu-id="923fe-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="923fe-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="923fe-123">Требования</span><span class="sxs-lookup"><span data-stu-id="923fe-123">Requirements</span></span>



| <span data-ttu-id="923fe-124">Требование</span><span class="sxs-lookup"><span data-stu-id="923fe-124">Requirement</span></span> | <span data-ttu-id="923fe-125">Значение</span><span class="sxs-lookup"><span data-stu-id="923fe-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="923fe-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="923fe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="923fe-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="923fe-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="923fe-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="923fe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="923fe-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="923fe-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="923fe-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="923fe-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="923fe-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923fe-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="923fe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="923fe-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="923fe-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923fe-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="923fe-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="923fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923fe-135">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="923fe-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





