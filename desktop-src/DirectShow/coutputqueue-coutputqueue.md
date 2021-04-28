---
description: Метод конструктора Каутпуткуеуе. Каутпуткуеуе.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Конструктор Каутпуткуеуе. Каутпуткуеуе (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095332"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="74348-103">Каутпуткуеуе. Каутпуткуеуе, конструктор</span><span class="sxs-lookup"><span data-stu-id="74348-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="74348-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="74348-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74348-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74348-105">Syntax</span></span>


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a><span data-ttu-id="74348-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74348-107">*пинпутпин*</span><span class="sxs-lookup"><span data-stu-id="74348-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="74348-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="74348-109">Объект будет доставлять примеры для этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="74348-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="74348-110">*фр*</span><span class="sxs-lookup"><span data-stu-id="74348-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-111">Указатель на код возврата **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74348-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="74348-112">\_Перед вызовом этого метода задайте для параметра значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="74348-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="74348-113">При возврате *фр* получает значение, указывающее на успешность или сбой метода.</span><span class="sxs-lookup"><span data-stu-id="74348-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="74348-114">*бауто*</span><span class="sxs-lookup"><span data-stu-id="74348-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-115">Флаг, указывающий, следует ли объекту создавать очередь.</span><span class="sxs-lookup"><span data-stu-id="74348-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="74348-116">Если **значение — true**, объект создает очередь только в том случае, если входной ПИН-код может быть заблокирован.</span><span class="sxs-lookup"><span data-stu-id="74348-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="74348-117">Если **значение равно false**, параметр *бкуеуе* указывает, следует ли создавать очередь.</span><span class="sxs-lookup"><span data-stu-id="74348-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="74348-118">*бкуеуе*</span><span class="sxs-lookup"><span data-stu-id="74348-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-119">Если *бауто* имеет **значение true**, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="74348-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="74348-120">Если *бауто* имеет **значение false**, этот флаг указывает, следует ли создавать очередь.</span><span class="sxs-lookup"><span data-stu-id="74348-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="74348-121">*лбатчсизе*</span><span class="sxs-lookup"><span data-stu-id="74348-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-122">Максимальное количество выборок для доставки в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="74348-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="74348-123">*ббатчексакт*</span><span class="sxs-lookup"><span data-stu-id="74348-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-124">Флаг, указывающий, следует ли использовать точные размеры пакетов.</span><span class="sxs-lookup"><span data-stu-id="74348-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="74348-125">Если **значение — true**, объект ожидает выборки *лбатчсизе* перед их доставкой во входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="74348-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="74348-126">Если **значение равно false**, объект доставляет примеры по мере их получения.</span><span class="sxs-lookup"><span data-stu-id="74348-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="74348-127">*ллистсизе*</span><span class="sxs-lookup"><span data-stu-id="74348-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-128">Размер кэша для очереди.</span><span class="sxs-lookup"><span data-stu-id="74348-128">Cache size for the queue.</span></span> <span data-ttu-id="74348-129">Значение по умолчанию DEFAULTCACHE. — константа, определенная для класса [**кбаселист**](cbaselist.md) .</span><span class="sxs-lookup"><span data-stu-id="74348-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="74348-130">*двприорити*</span><span class="sxs-lookup"><span data-stu-id="74348-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="74348-131">Приоритет потока, который доставляет образцы.</span><span class="sxs-lookup"><span data-stu-id="74348-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74348-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="74348-132">Remarks</span></span>

<span data-ttu-id="74348-133">Если *бауто* имеет **значение true**, объект вызывает метод [**имеминпутпин:: рецеивеканблокк**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) для подчиненного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="74348-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="74348-134">Если **рецеивеканблокк** возвращает значение S \_ ОК (означающее, что ПИН-код может блокироваться в вызовах [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ), объект создает поток для доставки образцов.</span><span class="sxs-lookup"><span data-stu-id="74348-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="74348-135">В противном случае он не создает поток.</span><span class="sxs-lookup"><span data-stu-id="74348-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="74348-136">Если *бауто* имеет значение **false**, *бкуеуе* определяет, следует ли создавать поток.</span><span class="sxs-lookup"><span data-stu-id="74348-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="74348-137">Если объект создает поток, он присваивает обработчику потока значение переменной-члена [**каутпуткуеуе:: m \_ хсреад**](coutputqueue-m-hthread.md) .</span><span class="sxs-lookup"><span data-stu-id="74348-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="74348-138">Потоковая процедура — [**каутпуткуеуе:: инитиалсреадпрок**](coutputqueue-initialthreadproc.md), а параметр Thread — это указатель на this.</span><span class="sxs-lookup"><span data-stu-id="74348-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="74348-139">Объект также создает очередь для хранения образцов, которая предоставляется переменной-членом [**\_ списка каутпуткуеуе:: m**](coutputqueue-m-list.md) .</span><span class="sxs-lookup"><span data-stu-id="74348-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="74348-140">Требования</span><span class="sxs-lookup"><span data-stu-id="74348-140">Requirements</span></span>



| <span data-ttu-id="74348-141">Требование</span><span class="sxs-lookup"><span data-stu-id="74348-141">Requirement</span></span> | <span data-ttu-id="74348-142">Значение</span><span class="sxs-lookup"><span data-stu-id="74348-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74348-143">Header</span><span class="sxs-lookup"><span data-stu-id="74348-143">Header</span></span><br/>  | <dl> <span data-ttu-id="74348-144"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74348-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="74348-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74348-145">Library</span></span><br/> | <dl> <span data-ttu-id="74348-146"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="74348-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74348-147">См. также</span><span class="sxs-lookup"><span data-stu-id="74348-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74348-148">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="74348-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




