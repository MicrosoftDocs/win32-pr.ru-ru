---
description: Метод Агримедиатипе выполняет поиск типа мультимедиа для создания подключения к ПИН-коду.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Кбасепин. Агримедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669311"
---
# <a name="cbasepinagreemediatype-method"></a><span data-ttu-id="cc9ca-103">Кбасепин. Агримедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="cc9ca-103">CBasePin.AgreeMediaType method</span></span>

<span data-ttu-id="cc9ca-104">`AgreeMediaType`Метод выполняет поиск типа носителя, чтобы установить подключение к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-104">The `AgreeMediaType` method searches for a media type to make a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc9ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc9ca-105">Syntax</span></span>


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="cc9ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc9ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc9ca-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="cc9ca-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="cc9ca-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) получающий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cc9ca-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="cc9ca-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="cc9ca-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies a media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc9ca-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc9ca-111">Return value</span></span>

<span data-ttu-id="cc9ca-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc9ca-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cc9ca-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="cc9ca-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cc9ca-114">Return code</span></span>                                                                                                  | <span data-ttu-id="cc9ca-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cc9ca-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="cc9ca-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ca-116"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="cc9ca-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="cc9ca-118"><dt>**VFW \_ E \_ нет \_ приемлемых \_ типов**</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ca-118"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="cc9ca-119">Не удалось найти допустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-119">No acceptable media type was found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cc9ca-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc9ca-120">Remarks</span></span>

<span data-ttu-id="cc9ca-121">Если параметр *ПЛТ* не равен **null** и полностью указывает тип носителя, этот метод пытается подключиться с помощью этого типа носителя.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-121">If the *pmt* parameter is non-**NULL** and fully specifies a media type, this method attempts a connection using that media type.</span></span> <span data-ttu-id="cc9ca-122">Если попытка не удалась, метод возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-122">If the attempt fails, the method returns an error.</span></span>

<span data-ttu-id="cc9ca-123">Если параметр *ПЛТ* имеет **значение NULL** или указывает на частичный тип носителя, этот метод пытается выполнить типы мультимедиа в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cc9ca-123">If the *pmt* parameter is **NULL** or specifies a partial media type, this method tries media types in the following order:</span></span>

1.  <span data-ttu-id="cc9ca-124">Предпочтительные типы носителей принимающего ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-124">The receiving pin's preferred media types.</span></span>
2.  <span data-ttu-id="cc9ca-125">Предпочтительные типы носителей для этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cc9ca-125">This pin's preferred media types.</span></span>

<span data-ttu-id="cc9ca-126">Предпочтительные типы мультимедиа перечисляются с помощью метода [**кбасепин:: енуммедиатипес**](cbasepin-enummediatypes.md) , а полученный перечислитель передается в метод [**Кбасепин:: тримедиатипес**](cbasepin-trymediatypes.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9ca-126">Preferred media types are enumerated with the [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) method, and the resulting enumerator is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9ca-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cc9ca-127">Requirements</span></span>



| <span data-ttu-id="cc9ca-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cc9ca-128">Requirement</span></span> | <span data-ttu-id="cc9ca-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cc9ca-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9ca-130">Header</span><span class="sxs-lookup"><span data-stu-id="cc9ca-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cc9ca-131"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ca-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc9ca-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc9ca-132">Library</span></span><br/> | <dl> <span data-ttu-id="cc9ca-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cc9ca-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc9ca-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc9ca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc9ca-135">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="cc9ca-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




