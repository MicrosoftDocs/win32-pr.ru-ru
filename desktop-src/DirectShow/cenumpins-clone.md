---
description: 'Метод Clone создает копию перечислителя с тем же состоянием перечисления. Этот метод реализует метод Иенумпинс:: Clone.'
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Метод Ценумпинс. Clone (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657582"
---
# <a name="cenumpinsclone-method"></a><span data-ttu-id="75d14-104">Ценумпинс. Clone, метод</span><span class="sxs-lookup"><span data-stu-id="75d14-104">CEnumPins.Clone method</span></span>

<span data-ttu-id="75d14-105">`Clone`Метод создает копию перечислителя с тем же состоянием перечисления.</span><span class="sxs-lookup"><span data-stu-id="75d14-105">The `Clone` method makes a copy of the enumerator with the same enumeration state.</span></span> <span data-ttu-id="75d14-106">Этот метод реализует метод [**иенумпинс:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .</span><span class="sxs-lookup"><span data-stu-id="75d14-106">This method implements the [**IEnumPins::Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d14-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75d14-107">Syntax</span></span>


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="75d14-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="75d14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d14-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="75d14-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="75d14-110">Адрес переменной, которая получает указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) нового перечислителя.</span><span class="sxs-lookup"><span data-stu-id="75d14-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of the new enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d14-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75d14-111">Return value</span></span>

<span data-ttu-id="75d14-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="75d14-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="75d14-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="75d14-113">Return code</span></span>                                                                                                | <span data-ttu-id="75d14-114">Описание</span><span class="sxs-lookup"><span data-stu-id="75d14-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75d14-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="75d14-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="75d14-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="75d14-116">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="75d14-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="75d14-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>              | <span data-ttu-id="75d14-118">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="75d14-118">Insufficient memory.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="75d14-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="75d14-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="75d14-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="75d14-120">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="75d14-121"><dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt></span><span class="sxs-lookup"><span data-stu-id="75d14-121"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="75d14-122">Состояние фильтра изменилось и теперь не согласуется с перечислителем.</span><span class="sxs-lookup"><span data-stu-id="75d14-122">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75d14-123">Требования</span><span class="sxs-lookup"><span data-stu-id="75d14-123">Requirements</span></span>



| <span data-ttu-id="75d14-124">Требование</span><span class="sxs-lookup"><span data-stu-id="75d14-124">Requirement</span></span> | <span data-ttu-id="75d14-125">Значение</span><span class="sxs-lookup"><span data-stu-id="75d14-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d14-126">Header</span><span class="sxs-lookup"><span data-stu-id="75d14-126">Header</span></span><br/>  | <dl> <span data-ttu-id="75d14-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75d14-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="75d14-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="75d14-128">Library</span></span><br/> | <dl> <span data-ttu-id="75d14-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="75d14-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d14-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75d14-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d14-131">**Класс Ценумпинс**</span><span class="sxs-lookup"><span data-stu-id="75d14-131">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




