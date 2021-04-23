---
description: Конструирует объект КМСГ.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Конструктор КМСГ. КМСГ (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675663"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="7280f-103">КМСГ. КМСГ, конструктор</span><span class="sxs-lookup"><span data-stu-id="7280f-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="7280f-104">Конструирует объект [**КМСГ**](cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="7280f-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7280f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7280f-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="7280f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7280f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7280f-107">*u*</span><span class="sxs-lookup"><span data-stu-id="7280f-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="7280f-108">Код запроса, определяемый клиентом класса потока и понятный переопределенной функцией рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="7280f-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="7280f-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="7280f-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="7280f-110">Параметр Flag для кода запроса.</span><span class="sxs-lookup"><span data-stu-id="7280f-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="7280f-111">*LP*</span><span class="sxs-lookup"><span data-stu-id="7280f-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="7280f-112">Указатель на данные, необходимые рабочему потоку в качестве параметра или возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="7280f-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="7280f-113">Эти данные не должны основываться на стеке, так как на них будет ссылка в течение некоторого времени после завершения операции очереди.</span><span class="sxs-lookup"><span data-stu-id="7280f-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="7280f-114">*певент*</span><span class="sxs-lookup"><span data-stu-id="7280f-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="7280f-115">Указатель на объект события, который может сообщить рабочему потоку для указания на завершение операции.</span><span class="sxs-lookup"><span data-stu-id="7280f-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7280f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7280f-116">Remarks</span></span>

<span data-ttu-id="7280f-117">Эта функция-член содержит запрос на выполнение рабочего потока [**кмсгсреад**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="7280f-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="7280f-118">Все параметры передаются в функцию рабочего потока в качестве параметров при обработке этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="7280f-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="7280f-119">Значения параметров определяются клиентской функцией, которая вызывает рабочий поток и производный класс, который предоставляет функцию выполнения рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="7280f-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7280f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7280f-120">Requirements</span></span>



| <span data-ttu-id="7280f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7280f-121">Requirement</span></span> | <span data-ttu-id="7280f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7280f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7280f-123">Header</span><span class="sxs-lookup"><span data-stu-id="7280f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7280f-124"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7280f-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7280f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7280f-125">Library</span></span><br/> | <dl> <span data-ttu-id="7280f-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7280f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




