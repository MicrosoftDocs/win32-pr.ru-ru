---
title: Метод Иконнектионброкеррекуест CheckStatus (Кбклиент. h)
description: Вызывается для определения состояния асинхронного запроса.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода CheckStatus
- Службы удаленных рабочих столов метода CheckStatus, интерфейс Иконнектионброкеррекуест
- Службы удаленных рабочих столов интерфейса Иконнектионброкеррекуест, метод CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416053"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="5e96c-106">Метод Иконнектионброкеррекуест:: CheckStatus</span><span class="sxs-lookup"><span data-stu-id="5e96c-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="5e96c-107">Вызывается для определения состояния асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="5e96c-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e96c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e96c-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5e96c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e96c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e96c-110">*прекстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5e96c-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e96c-111">Адрес переменной, получающей значение перечисления [**\_ \_ состояния запроса CB**](cb-request-status.md) , которое указывает состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="5e96c-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e96c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e96c-112">Return value</span></span>

<span data-ttu-id="5e96c-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e96c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e96c-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e96c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e96c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5e96c-115">Requirements</span></span>



| <span data-ttu-id="5e96c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5e96c-116">Requirement</span></span> | <span data-ttu-id="5e96c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5e96c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e96c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e96c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5e96c-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5e96c-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="5e96c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e96c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5e96c-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5e96c-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="5e96c-122">Header</span><span class="sxs-lookup"><span data-stu-id="5e96c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e96c-123"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e96c-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e96c-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e96c-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e96c-125"><dt>Кбклиент. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e96c-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e96c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5e96c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e96c-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e96c-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e96c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e96c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e96c-129">**иконнектионброкеррекуест**</span><span class="sxs-lookup"><span data-stu-id="5e96c-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





