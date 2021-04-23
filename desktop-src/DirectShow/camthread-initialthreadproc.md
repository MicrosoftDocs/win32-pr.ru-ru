---
description: Метод Инитиалсреадпрок вызывает основную процедуру потока.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Iniметод Тиалсреадпрок (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668960"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="a1c96-103">CAMThread.Iniметод Тиалсреадпрок</span><span class="sxs-lookup"><span data-stu-id="a1c96-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="a1c96-104">`InitialThreadProc`Метод вызывает основную процедуру потока.</span><span class="sxs-lookup"><span data-stu-id="a1c96-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1c96-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="a1c96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1c96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1c96-107">*PV*</span><span class="sxs-lookup"><span data-stu-id="a1c96-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="a1c96-108">`this` вид.</span><span class="sxs-lookup"><span data-stu-id="a1c96-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1c96-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1c96-109">Return value</span></span>

<span data-ttu-id="a1c96-110">Возвращает значение **типа DWORD** , возвращаемое функцией [**Камсреад:: среадпрок**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="a1c96-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="a1c96-111">Это значение определяется производным классом.</span><span class="sxs-lookup"><span data-stu-id="a1c96-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1c96-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1c96-112">Remarks</span></span>

<span data-ttu-id="a1c96-113">Метод [**камсреад:: Create**](camthread-create.md) использует этот метод для процедуры потока при создании потока.</span><span class="sxs-lookup"><span data-stu-id="a1c96-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="a1c96-114">В нем используется `this` указатель в качестве аргумента потока.</span><span class="sxs-lookup"><span data-stu-id="a1c96-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="a1c96-115">Этот метод вызывает метод [**камсреад:: коинитиализехелпер**](camthread-coinitializehelper.md) , а затем среадпрок.</span><span class="sxs-lookup"><span data-stu-id="a1c96-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c96-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a1c96-116">Requirements</span></span>



| <span data-ttu-id="a1c96-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a1c96-117">Requirement</span></span> | <span data-ttu-id="a1c96-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a1c96-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c96-119">Header</span><span class="sxs-lookup"><span data-stu-id="a1c96-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a1c96-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1c96-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a1c96-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a1c96-121">Library</span></span><br/> | <dl> <span data-ttu-id="a1c96-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a1c96-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c96-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1c96-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c96-124">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="a1c96-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




