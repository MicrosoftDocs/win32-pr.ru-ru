---
description: Метод Аттемптконнектион подключается к другому ПИН-коду с помощью указанного типа носителя.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Кбасепин. Аттемптконнектион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657970"
---
# <a name="cbasepinattemptconnection-method"></a><span data-ttu-id="7c365-103">Кбасепин. Аттемптконнектион, метод</span><span class="sxs-lookup"><span data-stu-id="7c365-103">CBasePin.AttemptConnection method</span></span>

<span data-ttu-id="7c365-104">`AttemptConnection`Метод подключается к другому ПИН-коду с помощью указанного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="7c365-104">The `AttemptConnection` method connects to another pin using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c365-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c365-105">Syntax</span></span>


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7c365-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c365-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="7c365-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7c365-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) получающий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="7c365-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7c365-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="7c365-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7c365-110">Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7c365-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c365-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c365-111">Return value</span></span>

<span data-ttu-id="7c365-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c365-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7c365-113">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7c365-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7c365-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7c365-114">Return code</span></span>                                                                                                | <span data-ttu-id="7c365-115">Описание</span><span class="sxs-lookup"><span data-stu-id="7c365-115">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7c365-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7c365-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="7c365-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7c365-117">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="7c365-118"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="7c365-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="7c365-119">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="7c365-119">The media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c365-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c365-120">Remarks</span></span>

<span data-ttu-id="7c365-121">Этот метод пытается подключить два контакта к определенному типу носителя.</span><span class="sxs-lookup"><span data-stu-id="7c365-121">This method attempts to connect the two pins with a specific media type.</span></span> <span data-ttu-id="7c365-122">Если тип является недопустимым, метод завершается с ошибкой, не пытаясь других типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7c365-122">If the type is not acceptable, the method fails without trying other media types.</span></span>

<span data-ttu-id="7c365-123">Если тип мультимедиа приемлем, этот метод вызывает метод [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) принимающего ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="7c365-123">If the media type is acceptable, this method calls the receiving pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="7c365-124">Затем вызывается метод [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md) для завершения соединения.</span><span class="sxs-lookup"><span data-stu-id="7c365-124">Then it calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method to complete the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c365-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7c365-125">Requirements</span></span>



| <span data-ttu-id="7c365-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7c365-126">Requirement</span></span> | <span data-ttu-id="7c365-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7c365-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c365-128">Header</span><span class="sxs-lookup"><span data-stu-id="7c365-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7c365-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c365-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7c365-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c365-130">Library</span></span><br/> | <dl> <span data-ttu-id="7c365-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7c365-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c365-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c365-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c365-133">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="7c365-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




