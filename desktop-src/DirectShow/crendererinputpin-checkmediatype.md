---
description: 'Метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя. Этот метод переопределяет метод Кбасепин:: Чеккмедиатипе.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Крендереринпутпин. Чеккмедиатипе, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657381"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="85b8e-104">Крендереринпутпин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="85b8e-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="85b8e-105">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="85b8e-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="85b8e-106">Этот метод переопределяет метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="85b8e-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85b8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85b8e-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="85b8e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85b8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b8e-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="85b8e-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="85b8e-110">Указатель на объект типа мультимедиа, который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="85b8e-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85b8e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85b8e-111">Return value</span></span>

<span data-ttu-id="85b8e-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85b8e-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b8e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="85b8e-113">Requirements</span></span>



| <span data-ttu-id="85b8e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="85b8e-114">Requirement</span></span> | <span data-ttu-id="85b8e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="85b8e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85b8e-116">Header</span><span class="sxs-lookup"><span data-stu-id="85b8e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="85b8e-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85b8e-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85b8e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85b8e-118">Library</span></span><br/> | <dl> <span data-ttu-id="85b8e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="85b8e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85b8e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85b8e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85b8e-121">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="85b8e-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




