---
description: При наличии списка типов мультимедиа метод Тримедиатипес пытается выполнить соединение, используя один из этих типов.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Кбасепин. Тримедиатипес, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657203"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="66314-103">Кбасепин. Тримедиатипес, метод</span><span class="sxs-lookup"><span data-stu-id="66314-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="66314-104">При наличии списка типов мультимедиа `TryMediaTypes` метод пытается выполнить соединение, используя один из этих типов.</span><span class="sxs-lookup"><span data-stu-id="66314-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="66314-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66314-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="66314-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66314-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66314-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="66314-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="66314-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) получающий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="66314-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="66314-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="66314-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="66314-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , ограничивающий возможные типы носителей, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="66314-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="66314-111">*пенум*</span><span class="sxs-lookup"><span data-stu-id="66314-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="66314-112">Указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , используемый для перечисления списка типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="66314-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66314-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66314-113">Return value</span></span>

<span data-ttu-id="66314-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66314-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="66314-115">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="66314-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="66314-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="66314-116">Return code</span></span>                                                                                                  | <span data-ttu-id="66314-117">Описание</span><span class="sxs-lookup"><span data-stu-id="66314-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="66314-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="66314-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="66314-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="66314-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="66314-120"><dt>**VFW \_ E \_ нет \_ приемлемых \_ типов**</dt></span><span class="sxs-lookup"><span data-stu-id="66314-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="66314-121">Не удалось найти допустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="66314-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66314-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66314-122">Remarks</span></span>

<span data-ttu-id="66314-123">Для каждого типа мультимедиа, возвращаемого интерфейсом **иенуммедиатипес** , этот метод пытается установить соединение, вызвав метод [**Кбасепин:: аттемптконнектион**](cbasepin-attemptconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="66314-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="66314-124">Если параметр *ПЛТ* не равен **null**, ПИН-код пропускает типы мультимедиа, которые не соответствуют этому типу.</span><span class="sxs-lookup"><span data-stu-id="66314-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="66314-125">Параметр *ПЛТ* может указывать частичный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="66314-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="66314-126">Частичный тип носителя имеет значение GUID \_ null для основного типа, подтипа или формата.</span><span class="sxs-lookup"><span data-stu-id="66314-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="66314-127">Значение GUID \_ null соответствует любому типу, аналогичному значению "подстановочный знак".</span><span class="sxs-lookup"><span data-stu-id="66314-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="66314-128">Требования</span><span class="sxs-lookup"><span data-stu-id="66314-128">Requirements</span></span>



| <span data-ttu-id="66314-129">Требование</span><span class="sxs-lookup"><span data-stu-id="66314-129">Requirement</span></span> | <span data-ttu-id="66314-130">Значение</span><span class="sxs-lookup"><span data-stu-id="66314-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66314-131">Header</span><span class="sxs-lookup"><span data-stu-id="66314-131">Header</span></span><br/>  | <dl> <span data-ttu-id="66314-132"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66314-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66314-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66314-133">Library</span></span><br/> | <dl> <span data-ttu-id="66314-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="66314-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66314-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66314-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66314-136">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="66314-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




