---
description: Метод конструктора Кдинамикаутпутпин. Кдинамикаутпутпин.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Конструктор Кдинамикаутпутпин. Кдинамикаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099312"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="c5170-103">Кдинамикаутпутпин. Кдинамикаутпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="c5170-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="c5170-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="c5170-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5170-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5170-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="c5170-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5170-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="c5170-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="c5170-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c5170-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="c5170-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="c5170-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5170-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="c5170-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="c5170-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="c5170-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="c5170-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="c5170-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="c5170-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="c5170-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="c5170-114">Используйте тот же критический раздел, что и для блокировки фильтра, [ **кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="c5170-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="c5170-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="c5170-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c5170-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="c5170-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="c5170-117">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="c5170-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="c5170-118">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="c5170-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="c5170-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="c5170-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c5170-120">Указатель на строку расширенных символов, содержащую идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c5170-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="c5170-121">Дополнительные сведения см. в разделе [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="c5170-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5170-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c5170-122">Requirements</span></span>



| <span data-ttu-id="c5170-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c5170-123">Requirement</span></span> | <span data-ttu-id="c5170-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c5170-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5170-125">Header</span><span class="sxs-lookup"><span data-stu-id="c5170-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c5170-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5170-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c5170-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5170-127">Library</span></span><br/> | <dl> <span data-ttu-id="c5170-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c5170-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5170-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c5170-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5170-130">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c5170-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




