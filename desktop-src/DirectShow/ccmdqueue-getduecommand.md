---
description: Метод Жетдуекомманд извлекает указатель на следующую команду из-за.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Ккмдкуеуе. Жетдуекомманд, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656892"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="2c3b5-103">Ккмдкуеуе. Жетдуекомманд, метод</span><span class="sxs-lookup"><span data-stu-id="2c3b5-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="2c3b5-104">`GetDueCommand`Метод получает указатель на следующую команду, которая вызвана.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c3b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c3b5-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="2c3b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c3b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c3b5-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="2c3b5-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="2c3b5-108">Адрес указателя на отложенную команду.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="2c3b5-109">*мстимеаут*</span><span class="sxs-lookup"><span data-stu-id="2c3b5-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="2c3b5-110">Время ожидания перед истечением времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c3b5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c3b5-111">Return value</span></span>

<span data-ttu-id="2c3b5-112">Возвращает значение "E \_ Abort", если истекло время ожидания.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="2c3b5-113">Возвращает значение \_ ОК, если выполнено успешно; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="2c3b5-114">Возвращает объект, который был увеличен с помощью **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c3b5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c3b5-115">Remarks</span></span>

<span data-ttu-id="2c3b5-116">Эта функция-член блокируется до тех пор, пока не будет вызвана Ожидающая команда.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="2c3b5-117">Функция члена блокирует количество времени в миллисекундах, указанное в параметре *мстимеаут* .</span><span class="sxs-lookup"><span data-stu-id="2c3b5-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="2c3b5-118">Команды времени потока становятся только между функциями-членами [**ккмдкуеуе:: Run**](ccmdqueue-run.md) и [**Ккмдкуеуе:: ендрун**](ccmdqueue-endrun.md) .</span><span class="sxs-lookup"><span data-stu-id="2c3b5-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="2c3b5-119">Команда остается в очереди до выполнения или отмены.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c3b5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2c3b5-120">Requirements</span></span>



| <span data-ttu-id="2c3b5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2c3b5-121">Requirement</span></span> | <span data-ttu-id="2c3b5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3b5-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3b5-123">Header</span><span class="sxs-lookup"><span data-stu-id="2c3b5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2c3b5-124"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c3b5-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c3b5-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c3b5-125">Library</span></span><br/> | <dl> <span data-ttu-id="2c3b5-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2c3b5-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c3b5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c3b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c3b5-128">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="2c3b5-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




