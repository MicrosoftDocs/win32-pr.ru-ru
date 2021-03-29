---
description: Блокируется до выхода из потока.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Кмсгсреад. Ваитфорсреадексит, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668889"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="1c85a-103">Кмсгсреад. Ваитфорсреадексит, метод</span><span class="sxs-lookup"><span data-stu-id="1c85a-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="1c85a-104">Блокируется до выхода из потока.</span><span class="sxs-lookup"><span data-stu-id="1c85a-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c85a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c85a-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="1c85a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c85a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c85a-107">*лпдвекситкоде*</span><span class="sxs-lookup"><span data-stu-id="1c85a-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="1c85a-108">Указатель на код выхода, возвращенный потоком.</span><span class="sxs-lookup"><span data-stu-id="1c85a-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c85a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c85a-109">Return value</span></span>

<span data-ttu-id="1c85a-110">Возвращает **значение true** или **false**, значение которого определяется классом, в котором указана Переопределенная функция-член [**кмсгсреад:: среадмессажепрок**](cmsgthread-threadmessageproc.md) и вызывающая функция-член.</span><span class="sxs-lookup"><span data-stu-id="1c85a-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c85a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c85a-111">Remarks</span></span>

<span data-ttu-id="1c85a-112">Перед завершением уничтожения производного класса убедитесь, что рабочий поток полностью завершил работу. в противном случае поток по-прежнему будет выполняться после выгрузки библиотеки динамической компоновки (DLL) из адресного пространства процесса.</span><span class="sxs-lookup"><span data-stu-id="1c85a-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="1c85a-113">Даже если только инструкция Left для Exit является инструкцией с одним возвратом, это вызовет исключение.</span><span class="sxs-lookup"><span data-stu-id="1c85a-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="1c85a-114">Единственный надежный способ убедиться в том, что поток завершил работу, — сообщить потоку о выходе (используя закрытый согласованный объект [**КМСГ**](cmsg.md) , отправленный в функцию-член [**Кмсгсреад::P утсреадмсг**](cmsgthread-putthreadmsg.md) ), а затем вызвать эту функцию-член.</span><span class="sxs-lookup"><span data-stu-id="1c85a-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="1c85a-115">Это следует сделать в деструкторе для производного класса.</span><span class="sxs-lookup"><span data-stu-id="1c85a-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c85a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1c85a-116">Requirements</span></span>



| <span data-ttu-id="1c85a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1c85a-117">Requirement</span></span> | <span data-ttu-id="1c85a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1c85a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c85a-119">Header</span><span class="sxs-lookup"><span data-stu-id="1c85a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1c85a-120"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c85a-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c85a-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c85a-121">Library</span></span><br/> | <dl> <span data-ttu-id="1c85a-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1c85a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c85a-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c85a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c85a-124">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="1c85a-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




