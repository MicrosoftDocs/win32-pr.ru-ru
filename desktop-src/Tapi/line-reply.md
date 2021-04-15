---
description: '\_Сообщение ответа линии TAPI отправляется для сообщения о результатах вызовов функций, выполненных асинхронно.'
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Сообщение LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689399"
---
# <a name="line_reply-message"></a><span data-ttu-id="39b63-103">\_Сообщение ответа строки</span><span class="sxs-lookup"><span data-stu-id="39b63-103">LINE\_REPLY message</span></span>

<span data-ttu-id="39b63-104">Сообщение **\_ ответа линии** TAPI отправляется для сообщения о результатах вызовов функций, выполненных асинхронно.</span><span class="sxs-lookup"><span data-stu-id="39b63-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="39b63-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="39b63-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b63-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="39b63-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="39b63-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="39b63-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="39b63-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="39b63-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="39b63-109">Возвращает экземпляр обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="39b63-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="39b63-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="39b63-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="39b63-111">Идентификатор запроса, для которого это ответ.</span><span class="sxs-lookup"><span data-stu-id="39b63-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="39b63-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="39b63-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="39b63-113">Индикатор успеха или ошибки.</span><span class="sxs-lookup"><span data-stu-id="39b63-113">The success or error indication.</span></span> <span data-ttu-id="39b63-114">Приложение должно привести этот параметр к типу LONG.</span><span class="sxs-lookup"><span data-stu-id="39b63-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="39b63-115">Ноль означает успешное завершение; отрицательное число указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="39b63-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="39b63-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="39b63-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="39b63-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="39b63-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b63-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39b63-118">Return value</span></span>

<span data-ttu-id="39b63-119">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="39b63-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b63-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39b63-120">Remarks</span></span>

<span data-ttu-id="39b63-121">Функции, которые работают асинхронно, возвращают положительное значение идентификатора запроса приложению.</span><span class="sxs-lookup"><span data-stu-id="39b63-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="39b63-122">Этот идентификатор запроса возвращается с ответным сообщением для идентификации завершенного запроса.</span><span class="sxs-lookup"><span data-stu-id="39b63-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="39b63-123">Другой параметр для сообщения **\_ ответа строки** содержит сведения об успешном или неудачном завершении.</span><span class="sxs-lookup"><span data-stu-id="39b63-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="39b63-124">Возможные ошибки те же, что определены соответствующей функцией.</span><span class="sxs-lookup"><span data-stu-id="39b63-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="39b63-125">Невозможно отключить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="39b63-125">This message cannot be disabled.</span></span>

<span data-ttu-id="39b63-126">В некоторых случаях приложение может не получить **\_ ответное сообщение строки** , соответствующее вызову асинхронной функции.</span><span class="sxs-lookup"><span data-stu-id="39b63-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="39b63-127">Это происходит, если соответствующий маркер вызова освобождается до получения сообщения.</span><span class="sxs-lookup"><span data-stu-id="39b63-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="39b63-128">Когда приложение вызывает любую асинхронную операцию, которая записывает данные обратно в память приложения, приложение должно обеспечить доступность памяти для записи, пока не будет получено сообщение **строки \_ Reply** или [**Line \_ гасердигитс**](line-gatherdigits.md) .</span><span class="sxs-lookup"><span data-stu-id="39b63-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39b63-129">Требования</span><span class="sxs-lookup"><span data-stu-id="39b63-129">Requirements</span></span>



| <span data-ttu-id="39b63-130">Требование</span><span class="sxs-lookup"><span data-stu-id="39b63-130">Requirement</span></span> | <span data-ttu-id="39b63-131">Значение</span><span class="sxs-lookup"><span data-stu-id="39b63-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="39b63-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="39b63-132">TAPI version</span></span><br/> | <span data-ttu-id="39b63-133">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="39b63-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="39b63-134">Header</span><span class="sxs-lookup"><span data-stu-id="39b63-134">Header</span></span><br/>       | <dl> <span data-ttu-id="39b63-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b63-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b63-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39b63-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b63-137">**Строка \_ гасердигитс**</span><span class="sxs-lookup"><span data-stu-id="39b63-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




