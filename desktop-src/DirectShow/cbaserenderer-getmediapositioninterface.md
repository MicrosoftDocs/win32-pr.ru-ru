---
description: Метод Жетмедиапоситионинтерфаце извлекает указатели интерфейса Имедиапоситион и Имедиасикинг фильтра.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Кбасерендерер. Жетмедиапоситионинтерфаце, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665301"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="ec5bb-103">Кбасерендерер. Жетмедиапоситионинтерфаце, метод</span><span class="sxs-lookup"><span data-stu-id="ec5bb-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="ec5bb-104">`GetMediaPositionInterface`Метод получает указатели интерфейса [**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) фильтра.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec5bb-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="ec5bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec5bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5bb-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="ec5bb-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5bb-108">Идентификатор ссылки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ec5bb-109">*ппв*</span><span class="sxs-lookup"><span data-stu-id="ec5bb-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5bb-110">Адрес переменной, получающей указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5bb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec5bb-111">Return value</span></span>

<span data-ttu-id="ec5bb-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec5bb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ec5bb-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ec5bb-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ec5bb-114">Return code</span></span>                                                                                   | <span data-ttu-id="ec5bb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ec5bb-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="ec5bb-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5bb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec5bb-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="ec5bb-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5bb-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec5bb-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="ec5bb-120"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5bb-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="ec5bb-121">Интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec5bb-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec5bb-122">Remarks</span></span>

<span data-ttu-id="ec5bb-123">Фильтр делегирует все команды поиска объекту [**крендерерпоспасссру**](crendererpospassthru.md) , который передает их восходящий поток.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="ec5bb-124">Этот метод создает объект **крендерерпоспасссру** , если он еще не существует, и запрашивает его для запрошенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ec5bb-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="ec5bb-125">В переменной-члене [**кбасерендерер:: m \_ ппоситион**](cbaserenderer-m-pposition.md) хранится указатель на объект **крендерерпоспасссру** .</span><span class="sxs-lookup"><span data-stu-id="ec5bb-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5bb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ec5bb-126">Requirements</span></span>



| <span data-ttu-id="ec5bb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ec5bb-127">Requirement</span></span> | <span data-ttu-id="ec5bb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ec5bb-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5bb-129">Header</span><span class="sxs-lookup"><span data-stu-id="ec5bb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ec5bb-130"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec5bb-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec5bb-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ec5bb-131">Library</span></span><br/> | <dl> <span data-ttu-id="ec5bb-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ec5bb-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5bb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec5bb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5bb-134">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="ec5bb-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




