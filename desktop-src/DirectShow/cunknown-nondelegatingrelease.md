---
description: 'Уменьшает значение счетчика ссылок на объект. Этот метод реализует метод Инонделегатингункновн:: Нонделегатингрелеасе.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Кункновн. Нонделегатингрелеасе, метод (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679692"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="036aa-104">Кункновн. Нонделегатингрелеасе, метод</span><span class="sxs-lookup"><span data-stu-id="036aa-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="036aa-105">Уменьшает значение счетчика ссылок на объект.</span><span class="sxs-lookup"><span data-stu-id="036aa-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="036aa-106">Этот метод реализует метод **инонделегатингункновн:: нонделегатингрелеасе** .</span><span class="sxs-lookup"><span data-stu-id="036aa-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="036aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="036aa-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="036aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="036aa-108">Parameters</span></span>

<span data-ttu-id="036aa-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="036aa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="036aa-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="036aa-110">Return value</span></span>

<span data-ttu-id="036aa-111">Возвращает счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="036aa-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="036aa-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="036aa-112">Remarks</span></span>

<span data-ttu-id="036aa-113">Когда счетчик ссылок достигает нуля, объект удаляет себя.</span><span class="sxs-lookup"><span data-stu-id="036aa-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="036aa-114">Требования</span><span class="sxs-lookup"><span data-stu-id="036aa-114">Requirements</span></span>



| <span data-ttu-id="036aa-115">Требование</span><span class="sxs-lookup"><span data-stu-id="036aa-115">Requirement</span></span> | <span data-ttu-id="036aa-116">Значение</span><span class="sxs-lookup"><span data-stu-id="036aa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="036aa-117">Header</span><span class="sxs-lookup"><span data-stu-id="036aa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="036aa-118"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="036aa-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="036aa-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="036aa-119">Library</span></span><br/> | <dl> <span data-ttu-id="036aa-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="036aa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




