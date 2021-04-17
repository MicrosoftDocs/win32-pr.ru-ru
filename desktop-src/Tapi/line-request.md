---
description: '\_Сообщение запроса линии TAPI отправляется, чтобы сообщить о поступлении нового запроса от другого приложения.'
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Сообщение LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685342"
---
# <a name="line_request-message"></a><span data-ttu-id="b31a2-103">\_Сообщение запроса строки</span><span class="sxs-lookup"><span data-stu-id="b31a2-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="b31a2-104">Сообщение **\_ запроса линии** TAPI отправляется, чтобы сообщить о поступлении нового запроса от другого приложения.</span><span class="sxs-lookup"><span data-stu-id="b31a2-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b31a2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b31a2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b31a2-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="b31a2-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b31a2-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b31a2-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b31a2-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="b31a2-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b31a2-109">Экземпляр регистрации приложения, указанного в [**линерегистеррекуестреЦипиент**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span><span class="sxs-lookup"><span data-stu-id="b31a2-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="b31a2-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b31a2-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b31a2-111">Режим запроса нового ожидающего запроса.</span><span class="sxs-lookup"><span data-stu-id="b31a2-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="b31a2-112">Этот параметр использует [**\_ константы линерекуестмоде**](linerequestmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b31a2-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b31a2-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b31a2-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b31a2-114">Условия для этого параметра —, если *dwParam1* имеет значение линерекуестмоде \_ Drop, *dwParam2* содержит *HWND* приложения, запрашивающего удаление.</span><span class="sxs-lookup"><span data-stu-id="b31a2-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="b31a2-115">В противном случае *dwParam2* не используется.</span><span class="sxs-lookup"><span data-stu-id="b31a2-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="b31a2-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b31a2-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b31a2-117">Если *dwParam1* имеет значение линерекуестмоде \_ Drop, то младшее слово *dwParam3* содержит *врекуестид* , как указано приложением, которое запросило удаление.</span><span class="sxs-lookup"><span data-stu-id="b31a2-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="b31a2-118">В противном случае *dwParam3* не используется.</span><span class="sxs-lookup"><span data-stu-id="b31a2-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b31a2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b31a2-119">Return value</span></span>

<span data-ttu-id="b31a2-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b31a2-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b31a2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b31a2-121">Remarks</span></span>

<span data-ttu-id="b31a2-122">Сообщение **\_ запроса строки** отправляется в приложение с наивысшим приоритетом, зарегистрированное для соответствующего режима запроса.</span><span class="sxs-lookup"><span data-stu-id="b31a2-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="b31a2-123">Это сообщение указывает на поступление запрошенной телефонной связи в указанном режиме запроса.</span><span class="sxs-lookup"><span data-stu-id="b31a2-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="b31a2-124">Если *dwParam1* — линерекуестмоде \_ MAKECALL, приложение может вызвать [**линежетрекуест**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) , используя соответствующий режим запроса для получения запроса.</span><span class="sxs-lookup"><span data-stu-id="b31a2-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="b31a2-125">Если *dwParam1* имеет значение линерекуестмоде \_ Drop, сообщение содержит все данные, необходимые получателю запроса для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="b31a2-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="b31a2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b31a2-126">Requirements</span></span>



| <span data-ttu-id="b31a2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b31a2-127">Requirement</span></span> | <span data-ttu-id="b31a2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b31a2-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b31a2-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b31a2-129">TAPI version</span></span><br/> | <span data-ttu-id="b31a2-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b31a2-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b31a2-131">Header</span><span class="sxs-lookup"><span data-stu-id="b31a2-131">Header</span></span><br/>       | <dl> <span data-ttu-id="b31a2-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b31a2-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b31a2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b31a2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b31a2-134">**линежетрекуест**</span><span class="sxs-lookup"><span data-stu-id="b31a2-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="b31a2-135">**линерегистеррекуестреЦипиент**</span><span class="sxs-lookup"><span data-stu-id="b31a2-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="b31a2-136">**тапирекуестмакекалл**</span><span class="sxs-lookup"><span data-stu-id="b31a2-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




