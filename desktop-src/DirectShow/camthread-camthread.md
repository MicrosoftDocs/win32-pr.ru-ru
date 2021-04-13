---
description: Метод конструктора.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Конструктор Камсреад. Камсреад (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657871"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="71279-103">Камсреад. Камсреад, конструктор</span><span class="sxs-lookup"><span data-stu-id="71279-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="71279-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="71279-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71279-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71279-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="71279-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71279-107">*фр*</span><span class="sxs-lookup"><span data-stu-id="71279-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="71279-108">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71279-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="71279-109">Если конструктор завершается неудачно, этот параметр получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="71279-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="71279-110">Если это происходит, объект находится в недопустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="71279-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="71279-111">Для обеспечения обратной совместимости с более ранними версиями стрмбасе. lib этот параметр по умолчанию **имеет значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="71279-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="71279-112">Однако рекомендуется передать значение, отличное от **null** , чтобы вызывающий объект мог проверить состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="71279-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71279-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71279-113">Remarks</span></span>

<span data-ttu-id="71279-114">Метод конструктора не создает поток.</span><span class="sxs-lookup"><span data-stu-id="71279-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="71279-115">Чтобы создать поток, вызовите метод [**камсреад:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="71279-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="71279-116">Требования</span><span class="sxs-lookup"><span data-stu-id="71279-116">Requirements</span></span>



| <span data-ttu-id="71279-117">Требование</span><span class="sxs-lookup"><span data-stu-id="71279-117">Requirement</span></span> | <span data-ttu-id="71279-118">Значение</span><span class="sxs-lookup"><span data-stu-id="71279-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71279-119">Header</span><span class="sxs-lookup"><span data-stu-id="71279-119">Header</span></span><br/>  | <dl> <span data-ttu-id="71279-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71279-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="71279-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71279-121">Library</span></span><br/> | <dl> <span data-ttu-id="71279-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="71279-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71279-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71279-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71279-124">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="71279-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




