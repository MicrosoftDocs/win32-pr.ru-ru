---
description: Считывает данные фильтра из заданного потока.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Кперсистстреам. Реадфромстреам, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668667"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="8e379-103">Кперсистстреам. Реадфромстреам, метод</span><span class="sxs-lookup"><span data-stu-id="8e379-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="8e379-104">Считывает данные фильтра из заданного потока.</span><span class="sxs-lookup"><span data-stu-id="8e379-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e379-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e379-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="8e379-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e379-107">*пстреам*</span><span class="sxs-lookup"><span data-stu-id="8e379-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="8e379-108">Указатель на интерфейс **IStream** , из которого считываются данные.</span><span class="sxs-lookup"><span data-stu-id="8e379-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e379-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e379-109">Return value</span></span>

<span data-ttu-id="8e379-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8e379-110">Returns S\_OK.</span></span> <span data-ttu-id="8e379-111">Производный класс должен возвращать допустимое значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e379-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e379-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e379-112">Remarks</span></span>

<span data-ttu-id="8e379-113">Версия по умолчанию не считывает ничего; его можно переопределить для чтения данных, относящихся к вашему классу.</span><span class="sxs-lookup"><span data-stu-id="8e379-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e379-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8e379-114">Requirements</span></span>



| <span data-ttu-id="8e379-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8e379-115">Requirement</span></span> | <span data-ttu-id="8e379-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e379-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e379-117">Header</span><span class="sxs-lookup"><span data-stu-id="8e379-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e379-118"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e379-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e379-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e379-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e379-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8e379-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e379-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e379-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e379-122">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="8e379-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




