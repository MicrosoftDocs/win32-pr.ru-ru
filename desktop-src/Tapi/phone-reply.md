---
description: '\_Ответное сообщение Phone TAPI отправляется в приложение для передачи результатов вызова функции, выполненного асинхронно.'
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Сообщение PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685059"
---
# <a name="phone_reply-message"></a><span data-ttu-id="ff97d-103">\_Ответное сообщение для телефона</span><span class="sxs-lookup"><span data-stu-id="ff97d-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="ff97d-104">**\_ Ответное сообщение Phone** TAPI отправляется в приложение для передачи результатов вызова функции, выполненного асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ff97d-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ff97d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff97d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff97d-106">*хфоне*</span><span class="sxs-lookup"><span data-stu-id="ff97d-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="ff97d-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ff97d-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="ff97d-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="ff97d-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ff97d-109">Возвращает экземпляр обратного вызова приложения.</span><span class="sxs-lookup"><span data-stu-id="ff97d-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="ff97d-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ff97d-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ff97d-111">Идентификатор запроса, для которого это ответ.</span><span class="sxs-lookup"><span data-stu-id="ff97d-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="ff97d-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ff97d-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ff97d-113">Индикатор успеха или ошибки.</span><span class="sxs-lookup"><span data-stu-id="ff97d-113">The success or error indication.</span></span> <span data-ttu-id="ff97d-114">Приложение должно привести этот параметр к типу LONG.</span><span class="sxs-lookup"><span data-stu-id="ff97d-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="ff97d-115">Ноль означает успешное завершение; отрицательное число указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ff97d-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="ff97d-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ff97d-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ff97d-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ff97d-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff97d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff97d-118">Return value</span></span>

<span data-ttu-id="ff97d-119">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ff97d-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff97d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff97d-120">Remarks</span></span>

<span data-ttu-id="ff97d-121">Функции, которые работают асинхронно, возвращают положительное значение идентификатора запроса приложению.</span><span class="sxs-lookup"><span data-stu-id="ff97d-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="ff97d-122">Этот идентификатор запроса возвращается с ответным сообщением для идентификации завершенного запроса.</span><span class="sxs-lookup"><span data-stu-id="ff97d-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="ff97d-123">Другой параметр для **\_ ответного сообщения Phone** содержит сведения об успешном или неудачном завершении.</span><span class="sxs-lookup"><span data-stu-id="ff97d-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="ff97d-124">Возможные ошибки те же, что определены соответствующей функцией.</span><span class="sxs-lookup"><span data-stu-id="ff97d-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="ff97d-125">Невозможно отключить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ff97d-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff97d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ff97d-126">Requirements</span></span>



| <span data-ttu-id="ff97d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ff97d-127">Requirement</span></span> | <span data-ttu-id="ff97d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ff97d-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ff97d-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ff97d-129">TAPI version</span></span><br/> | <span data-ttu-id="ff97d-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ff97d-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ff97d-131">Header</span><span class="sxs-lookup"><span data-stu-id="ff97d-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ff97d-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff97d-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




