---
description: Метод конструктора.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Конструктор Кмсгсреад. Кмсгсреад (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675661"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="f8126-103">Кмсгсреад. Кмсгсреад, конструктор</span><span class="sxs-lookup"><span data-stu-id="f8126-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="f8126-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f8126-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8126-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8126-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="f8126-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8126-106">Parameters</span></span>

<span data-ttu-id="f8126-107">Этот конструктор не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f8126-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8126-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8126-108">Remarks</span></span>

<span data-ttu-id="f8126-109">Создание объекта потока сообщений не приводит к автоматическому созданию потока.</span><span class="sxs-lookup"><span data-stu-id="f8126-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="f8126-110">Для создания потока необходимо вызвать функцию члена [**кмсгсреад:: CreateThread**](cmsgthread-createthread.md) .</span><span class="sxs-lookup"><span data-stu-id="f8126-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8126-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f8126-111">Requirements</span></span>



| <span data-ttu-id="f8126-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f8126-112">Requirement</span></span> | <span data-ttu-id="f8126-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f8126-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8126-114">Header</span><span class="sxs-lookup"><span data-stu-id="f8126-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f8126-115"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8126-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8126-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8126-116">Library</span></span><br/> | <dl> <span data-ttu-id="f8126-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f8126-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8126-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8126-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8126-119">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="f8126-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




