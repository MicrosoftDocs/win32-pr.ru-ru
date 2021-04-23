---
description: Функция Креатепоспасссру создает объект Кпоспасссру или Крендерерпоспасссру.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Функция Креатепоспасссру (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679676"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="041c5-103">Функция Креатепоспасссру</span><span class="sxs-lookup"><span data-stu-id="041c5-103">CreatePosPassThru function</span></span>

<span data-ttu-id="041c5-104">`CreatePosPassThru`Функция создает объект [**Кпоспасссру**](cpospassthru.md) или [**крендерерпоспасссру**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="041c5-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="041c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="041c5-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="041c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="041c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="041c5-107">*пагг*</span><span class="sxs-lookup"><span data-stu-id="041c5-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="041c5-108">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="041c5-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="041c5-109">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="041c5-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="041c5-110">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="041c5-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="041c5-111">*брендерер*</span><span class="sxs-lookup"><span data-stu-id="041c5-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="041c5-112">Логическое значение, указывающее, является ли фильтр модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="041c5-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="041c5-113">Используйте значение **true** , если фильтр является модулем подготовки отчетов, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="041c5-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="041c5-114">Если значение равно **true**, этот метод создает экземпляр класса [**крендерерпоспасссру**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="041c5-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="041c5-115">Если значение равно **false**, метод создает экземпляр класса **кпоспасссру** .</span><span class="sxs-lookup"><span data-stu-id="041c5-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="041c5-116">*ппин*</span><span class="sxs-lookup"><span data-stu-id="041c5-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="041c5-117">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) для входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="041c5-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="041c5-118">*пппасссру*</span><span class="sxs-lookup"><span data-stu-id="041c5-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="041c5-119">Адрес переменной, которая получает указатель на интерфейс **IUnknown** объекта.</span><span class="sxs-lookup"><span data-stu-id="041c5-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="041c5-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="041c5-120">Return value</span></span>

<span data-ttu-id="041c5-121">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="041c5-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="041c5-122">В противном случае возвращает значение **HRESULT** , указывающее причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="041c5-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="041c5-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="041c5-123">Remarks</span></span>

<span data-ttu-id="041c5-124">Этот метод использует интерфейс [**исикингпасссру**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="041c5-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="041c5-125">Объект загружается динамически из Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="041c5-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="041c5-126">Если функция выполнена успешно, возвращенный интерфейс **IUnknown** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="041c5-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="041c5-127">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="041c5-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="041c5-128">Требования</span><span class="sxs-lookup"><span data-stu-id="041c5-128">Requirements</span></span>



| <span data-ttu-id="041c5-129">Требование</span><span class="sxs-lookup"><span data-stu-id="041c5-129">Requirement</span></span> | <span data-ttu-id="041c5-130">Значение</span><span class="sxs-lookup"><span data-stu-id="041c5-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="041c5-131">Header</span><span class="sxs-lookup"><span data-stu-id="041c5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="041c5-132"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="041c5-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="041c5-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="041c5-133">Library</span></span><br/> | <dl> <span data-ttu-id="041c5-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="041c5-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="041c5-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="041c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041c5-136">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="041c5-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




