---
description: 'Метод Clone создает копию перечислителя с тем же состоянием перечисления. Этот метод реализует метод Иенуммедиатипес:: Clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Метод Ценуммедиатипес. Clone (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668831"
---
# <a name="cenummediatypesclone-method"></a><span data-ttu-id="5d306-104">Ценуммедиатипес. Clone, метод</span><span class="sxs-lookup"><span data-stu-id="5d306-104">CEnumMediaTypes.Clone method</span></span>

<span data-ttu-id="5d306-105">`Clone`Метод создает копию перечислителя с тем же состоянием перечисления.</span><span class="sxs-lookup"><span data-stu-id="5d306-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="5d306-106">Этот метод реализует метод [**иенуммедиатипес:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .</span><span class="sxs-lookup"><span data-stu-id="5d306-106">This method implements the [**IEnumMediaTypes::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d306-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d306-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5d306-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d306-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d306-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="5d306-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="5d306-110">Адрес переменной, которая получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) нового перечислителя.</span><span class="sxs-lookup"><span data-stu-id="5d306-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d306-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d306-111">Return value</span></span>

<span data-ttu-id="5d306-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5d306-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5d306-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d306-113">Return code</span></span>                                                                                                | <span data-ttu-id="5d306-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5d306-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d306-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5d306-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="5d306-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5d306-116">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="5d306-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5d306-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="5d306-118">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="5d306-118">Insufficient memory.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="5d306-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d306-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="5d306-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="5d306-120">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="5d306-121"><dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt></span><span class="sxs-lookup"><span data-stu-id="5d306-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="5d306-122">Состояние ПИН-кода изменилось и теперь не согласуется с перечислителем.</span><span class="sxs-lookup"><span data-stu-id="5d306-122">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d306-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5d306-123">Requirements</span></span>



| <span data-ttu-id="5d306-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5d306-124">Requirement</span></span> | <span data-ttu-id="5d306-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5d306-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d306-126">Header</span><span class="sxs-lookup"><span data-stu-id="5d306-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5d306-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d306-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5d306-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d306-128">Library</span></span><br/> | <dl> <span data-ttu-id="5d306-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5d306-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d306-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d306-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d306-131">**Класс Ценуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="5d306-131">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




