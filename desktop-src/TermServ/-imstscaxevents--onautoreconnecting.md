---
title: Имстскаксевентс Онаутореконнектинг, метод
description: Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов). | Имстскаксевентс Онаутореконнектинг, метод
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаутореконнектинг
- Службы удаленных рабочих столов метода Онаутореконнектинг, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онаутореконнектинг
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353485"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="22e54-107">Метод Имстскаксевентс:: Онаутореконнектинг</span><span class="sxs-lookup"><span data-stu-id="22e54-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="22e54-108">Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="22e54-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e54-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22e54-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="22e54-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="22e54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e54-111">*дисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22e54-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e54-112">Код, описывающий причину последнего отключения сеанса.</span><span class="sxs-lookup"><span data-stu-id="22e54-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="22e54-113">*аттемпткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22e54-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e54-114">Число попыток, выполненных в текущем процессе автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="22e54-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="22e54-115">Это число увеличивается на единицу при каждой попытке.</span><span class="sxs-lookup"><span data-stu-id="22e54-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="22e54-116">*паркконтинуестатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22e54-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22e54-117">Указатель на возвращаемый код, указывающий состояние автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="22e54-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="22e54-118">Этот код можно сбросить, чтобы изменить состояние текущего процесса автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="22e54-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="22e54-119">Дополнительные сведения о сбросе этого кода см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="22e54-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="22e54-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>Аутореконнектконтинуеаутоматик \* \* \* \* (0)</span><span class="sxs-lookup"><span data-stu-id="22e54-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="22e54-121">Процесс повторного подключения происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="22e54-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="22e54-122">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22e54-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="22e54-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>Аутореконнектконтинуестоп \* \* \* \* (1)</span><span class="sxs-lookup"><span data-stu-id="22e54-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="22e54-124">Процесс повторного подключения остановлен.</span><span class="sxs-lookup"><span data-stu-id="22e54-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="22e54-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>Аутореконнектконтинуемануал \* \* \* \* (2)</span><span class="sxs-lookup"><span data-stu-id="22e54-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="22e54-126">Процесс повторного подключения происходит вручную.</span><span class="sxs-lookup"><span data-stu-id="22e54-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e54-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22e54-127">Return value</span></span>

<span data-ttu-id="22e54-128">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="22e54-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22e54-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22e54-129">Remarks</span></span>

<span data-ttu-id="22e54-130">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что элемент управления переустанавливает подключение к серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="22e54-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="22e54-131">При изменении состояния автоматического повторного подключения путем присвоения параметру *паркконтинуестатус* значения **аутореконнектконтинуеаутоматик** этот метод работает в режиме чистого консультационного режима.</span><span class="sxs-lookup"><span data-stu-id="22e54-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="22e54-132">Контейнеры могут прослушивать это событие для уведомлений о том, что процесс автоматического повторного подключения продолжается.</span><span class="sxs-lookup"><span data-stu-id="22e54-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="22e54-133">Элемент управления автоматически пытается восстановить соединение на основе его внутреннего времени и количества попыток.</span><span class="sxs-lookup"><span data-stu-id="22e54-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="22e54-134">Этот метод вызывается во время каждой попытки автоматического повторного подключения, чтобы уведомить контейнер.</span><span class="sxs-lookup"><span data-stu-id="22e54-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="22e54-135">Когда состояние автоматического повторного подключения изменяется путем установки для параметра *паркконтинуестатус* значения **аутореконнектконтинуестоп**, текущая попытка автоматического повторного подключения будет прервана, уведомление об отключении будет отправлено в контейнер, а последующие уведомления не будут выдаваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="22e54-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="22e54-136">Чтобы включить или отключить автоматическое повторное подключение, используйте свойство [**енаблеаутореконнект**](imsrdpclientadvancedsettings2-enableautoreconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="22e54-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="22e54-137">Когда состояние автоматического повторного подключения изменяется путем установки для параметра *паркконтинуестатус* значения **аутореконнектконтинуемануал**, контейнер будет вручную управлять процессом автоматического повторного подключения, вызывая [**Connect**](imstscax-connect.md) для активации попытки подключения или [**отключения**](imstscax-disconnect.md) для отмены автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="22e54-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="22e54-138">После установки этого значения элемент управления прекращает выполнять автоматические попытки повторного подключения и становится политикой контейнера, чтобы вызовы Connect для активации автоматических **повторных** попыток подключения.</span><span class="sxs-lookup"><span data-stu-id="22e54-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="22e54-139">Это делается, когда контейнер предоставляет настраиваемое поведение пользовательского интерфейса для автоматического повторного подключения, например перезапуск удаленного подключения RAS или VPN-соединения перед автоматическим повторным подключением.</span><span class="sxs-lookup"><span data-stu-id="22e54-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="22e54-140">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="22e54-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22e54-141">Требования</span><span class="sxs-lookup"><span data-stu-id="22e54-141">Requirements</span></span>



| <span data-ttu-id="22e54-142">Требование</span><span class="sxs-lookup"><span data-stu-id="22e54-142">Requirement</span></span> | <span data-ttu-id="22e54-143">Значение</span><span class="sxs-lookup"><span data-stu-id="22e54-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22e54-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22e54-144">Minimum supported client</span></span><br/> | <span data-ttu-id="22e54-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22e54-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="22e54-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22e54-146">Minimum supported server</span></span><br/> | <span data-ttu-id="22e54-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22e54-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="22e54-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="22e54-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="22e54-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e54-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="22e54-150">DLL</span><span class="sxs-lookup"><span data-stu-id="22e54-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22e54-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e54-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e54-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22e54-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e54-153">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="22e54-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





