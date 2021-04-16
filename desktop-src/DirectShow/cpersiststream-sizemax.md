---
description: Возвращает максимальный размер в байтах, необходимый для текущего потока, не включая номер версии.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Кперсистстреам. Сиземакс, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668665"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="88dd5-103">Кперсистстреам. Сиземакс, метод</span><span class="sxs-lookup"><span data-stu-id="88dd5-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="88dd5-104">Возвращает максимальный размер в байтах, необходимый для текущего потока, не включая номер версии.</span><span class="sxs-lookup"><span data-stu-id="88dd5-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dd5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88dd5-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="88dd5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88dd5-106">Parameters</span></span>

<span data-ttu-id="88dd5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="88dd5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88dd5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88dd5-108">Return value</span></span>

<span data-ttu-id="88dd5-109">Возвращает число байтов, необходимых для данных, не включая номер версии.</span><span class="sxs-lookup"><span data-stu-id="88dd5-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="88dd5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88dd5-110">Remarks</span></span>

<span data-ttu-id="88dd5-111">Версия по умолчанию возвращает нуль. Он должен быть переопределен для предоставления другого подходящего значения.</span><span class="sxs-lookup"><span data-stu-id="88dd5-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="88dd5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="88dd5-112">Requirements</span></span>



| <span data-ttu-id="88dd5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="88dd5-113">Requirement</span></span> | <span data-ttu-id="88dd5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="88dd5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88dd5-115">Header</span><span class="sxs-lookup"><span data-stu-id="88dd5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="88dd5-116"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88dd5-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88dd5-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88dd5-117">Library</span></span><br/> | <dl> <span data-ttu-id="88dd5-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="88dd5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88dd5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88dd5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dd5-120">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="88dd5-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




