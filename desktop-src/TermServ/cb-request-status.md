---
title: Перечисление CB_REQUEST_STATUS (Кбклиент. h)
description: Указывает состояние асинхронного запроса.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Перечисление CB_REQUEST_STATUS службы удаленных рабочих столов
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340535"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="ae3fd-104">\_ \_ Перечисление состояния запросов CB</span><span class="sxs-lookup"><span data-stu-id="ae3fd-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="ae3fd-105">Указывает состояние асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="ae3fd-106">Это перечисление используется с методом [**иконнектионброкеррекуест:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="ae3fd-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae3fd-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="ae3fd-108">Константы</span><span class="sxs-lookup"><span data-stu-id="ae3fd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ae3fd-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_состояние CB \_ недопустимо**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-110">Объект запроса не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_запрос на \_ инициирование состояния CB \_**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_запрос состояния \_ CB \_ выполнен**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-114">Запрос завершен.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_ \_ сбой запроса состояния \_ CB**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-116">Ошибка запроса.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_запрос состояния \_ CB \_ прерван**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-118">Запрос был прерван.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_состояние CB \_ Поиск \_ места назначения**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_назначение " \_ Загрузка \_ состояния CB"**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**\_состояние CB \_ перевод \_ сеанса в \_ режим «в сети»**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae3fd-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_состояние CB \_ Перенаправление \_ на \_ место назначения**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="ae3fd-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae3fd-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae3fd-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ae3fd-127">Requirements</span></span>



| <span data-ttu-id="ae3fd-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ae3fd-128">Requirement</span></span> | <span data-ttu-id="ae3fd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ae3fd-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3fd-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae3fd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ae3fd-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ae3fd-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="ae3fd-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae3fd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ae3fd-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae3fd-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="ae3fd-134">Header</span><span class="sxs-lookup"><span data-stu-id="ae3fd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae3fd-135"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3fd-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae3fd-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae3fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3fd-137">**Иконнектионброкеррекуест:: CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="ae3fd-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





