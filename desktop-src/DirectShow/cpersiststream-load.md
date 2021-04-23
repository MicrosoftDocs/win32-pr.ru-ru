---
description: Загружает данные фильтра из заданного потока.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Метод Кперсистстреам. Load (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668668"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="729fa-103">Кперсистстреам. Load, метод</span><span class="sxs-lookup"><span data-stu-id="729fa-103">CPersistStream.Load method</span></span>

<span data-ttu-id="729fa-104">Загружает данные фильтра из заданного потока.</span><span class="sxs-lookup"><span data-stu-id="729fa-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="729fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="729fa-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="729fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="729fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="729fa-107">*пстм*</span><span class="sxs-lookup"><span data-stu-id="729fa-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="729fa-108">Указатель на поток, из которого будет загружен объект.</span><span class="sxs-lookup"><span data-stu-id="729fa-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="729fa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="729fa-109">Return value</span></span>

<span data-ttu-id="729fa-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="729fa-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="729fa-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="729fa-111">Remarks</span></span>

<span data-ttu-id="729fa-112">Эта функция члена реализует метод **IPersistStream:: Load** .</span><span class="sxs-lookup"><span data-stu-id="729fa-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="729fa-113">Требования</span><span class="sxs-lookup"><span data-stu-id="729fa-113">Requirements</span></span>



| <span data-ttu-id="729fa-114">Требование</span><span class="sxs-lookup"><span data-stu-id="729fa-114">Requirement</span></span> | <span data-ttu-id="729fa-115">Значение</span><span class="sxs-lookup"><span data-stu-id="729fa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="729fa-116">Header</span><span class="sxs-lookup"><span data-stu-id="729fa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="729fa-117"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="729fa-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="729fa-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="729fa-118">Library</span></span><br/> | <dl> <span data-ttu-id="729fa-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="729fa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="729fa-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="729fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="729fa-121">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="729fa-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




