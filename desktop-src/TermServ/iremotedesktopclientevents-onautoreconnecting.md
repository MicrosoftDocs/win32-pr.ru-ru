---
title: Иремотедесктопклиентевентс Онаутореконнектинг, метод
description: Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онаутореконнектинг
- Службы удаленных рабочих столов метода Онаутореконнектинг, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Онаутореконнектинг
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535393"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="6372c-106">Метод Иремотедесктопклиентевентс:: Онаутореконнектинг</span><span class="sxs-lookup"><span data-stu-id="6372c-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="6372c-107">Вызывается, когда клиентский элемент управления пытается автоматически восстановить соединение с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="6372c-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="6372c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6372c-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="6372c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6372c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6372c-110">*дисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6372c-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6372c-111">Причина события Disconnect.</span><span class="sxs-lookup"><span data-stu-id="6372c-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="6372c-112">*Екстендеддисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6372c-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6372c-113">Расширенные сведения о событии Disconnect.</span><span class="sxs-lookup"><span data-stu-id="6372c-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="6372c-114">*дисконнектеррормессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6372c-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6372c-115">Сообщение об ошибке для события Disconnect.</span><span class="sxs-lookup"><span data-stu-id="6372c-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="6372c-116">*нетворкаваилабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6372c-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6372c-117">Доступна ли сеть.</span><span class="sxs-lookup"><span data-stu-id="6372c-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="6372c-118">*аттемпткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6372c-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6372c-119">В этом случае это.</span><span class="sxs-lookup"><span data-stu-id="6372c-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="6372c-120">*максаттемпткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6372c-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6372c-121">Будет выполнено максимальное число попыток повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="6372c-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6372c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6372c-122">Return value</span></span>

<span data-ttu-id="6372c-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6372c-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6372c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6372c-124">Requirements</span></span>



| <span data-ttu-id="6372c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6372c-125">Requirement</span></span> | <span data-ttu-id="6372c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6372c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6372c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6372c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6372c-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6372c-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="6372c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6372c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6372c-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6372c-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="6372c-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6372c-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="6372c-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6372c-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6372c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6372c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6372c-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6372c-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6372c-135">IID</span><span class="sxs-lookup"><span data-stu-id="6372c-135">IID</span></span><br/>                      | <span data-ttu-id="6372c-136">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="6372c-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6372c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6372c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6372c-138">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="6372c-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





