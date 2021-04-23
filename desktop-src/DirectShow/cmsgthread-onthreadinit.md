---
description: Обеспечивает инициализацию потока.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Кмсгсреад. Онсреадинит, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675120"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="79d4c-103">Кмсгсреад. Онсреадинит, метод</span><span class="sxs-lookup"><span data-stu-id="79d4c-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="79d4c-104">Обеспечивает инициализацию потока.</span><span class="sxs-lookup"><span data-stu-id="79d4c-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79d4c-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="79d4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79d4c-106">Parameters</span></span>

<span data-ttu-id="79d4c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="79d4c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79d4c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79d4c-108">Return value</span></span>

<span data-ttu-id="79d4c-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="79d4c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79d4c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79d4c-110">Remarks</span></span>

<span data-ttu-id="79d4c-111">Переопределите эту функцию, если вы хотите выполнить собственную инициализацию при запуске потока.</span><span class="sxs-lookup"><span data-stu-id="79d4c-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d4c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="79d4c-112">Requirements</span></span>



| <span data-ttu-id="79d4c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="79d4c-113">Requirement</span></span> | <span data-ttu-id="79d4c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="79d4c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79d4c-115">Header</span><span class="sxs-lookup"><span data-stu-id="79d4c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="79d4c-116"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79d4c-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79d4c-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79d4c-117">Library</span></span><br/> | <dl> <span data-ttu-id="79d4c-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="79d4c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d4c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79d4c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d4c-120">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="79d4c-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




