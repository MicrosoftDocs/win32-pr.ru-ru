---
description: 'Метод Жеталлокаторрекуирементс извлекает свойства распределителя, запрошенные ПИН-кодом. Этот метод реализует метод Имеминпутпин:: Жеталлокаторрекуирементс.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Ктрансинплацеинпутпин. Жеталлокаторрекуирементс, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676052"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="55283-104">Ктрансинплацеинпутпин. Жеталлокаторрекуирементс, метод</span><span class="sxs-lookup"><span data-stu-id="55283-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="55283-105">`GetAllocatorRequirements`Метод получает свойства распределителя, запрошенные ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="55283-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="55283-106">Этот метод реализует метод [**имеминпутпин:: жеталлокаторрекуирементс**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .</span><span class="sxs-lookup"><span data-stu-id="55283-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55283-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55283-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="55283-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="55283-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55283-109">*ппропс*</span><span class="sxs-lookup"><span data-stu-id="55283-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="55283-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая заполняется требованиями.</span><span class="sxs-lookup"><span data-stu-id="55283-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55283-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55283-111">Return value</span></span>

<span data-ttu-id="55283-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55283-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="55283-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55283-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="55283-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="55283-114">Return code</span></span>                                                                               | <span data-ttu-id="55283-115">Описание</span><span class="sxs-lookup"><span data-stu-id="55283-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55283-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="55283-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="55283-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="55283-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="55283-118"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="55283-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="55283-119">Выходной ПИН-код не подключен, или его входной ПИН-код не поддерживает метод.</span><span class="sxs-lookup"><span data-stu-id="55283-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="55283-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="55283-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="55283-121">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="55283-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="55283-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55283-122">Remarks</span></span>

<span data-ttu-id="55283-123">Если выходной ПИН-код подключен, этот метод передает вызов нисходящего входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="55283-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="55283-124">В противном случае возвращается E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="55283-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="55283-125">Требования</span><span class="sxs-lookup"><span data-stu-id="55283-125">Requirements</span></span>



| <span data-ttu-id="55283-126">Требование</span><span class="sxs-lookup"><span data-stu-id="55283-126">Requirement</span></span> | <span data-ttu-id="55283-127">Значение</span><span class="sxs-lookup"><span data-stu-id="55283-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55283-128">Header</span><span class="sxs-lookup"><span data-stu-id="55283-128">Header</span></span><br/>  | <dl> <span data-ttu-id="55283-129"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55283-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55283-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55283-130">Library</span></span><br/> | <dl> <span data-ttu-id="55283-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="55283-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55283-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55283-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55283-133">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="55283-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




