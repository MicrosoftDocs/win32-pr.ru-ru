---
description: 'Метод QueryId извлекает идентификатор для ПИН-кода. Этот метод реализует метод Ипин:: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Ктрансформинпутпин. QueryId, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daae425e82bbc89cfbc863baea1924e36e63f122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675843"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="87083-104">Ктрансформинпутпин. QueryId, метод</span><span class="sxs-lookup"><span data-stu-id="87083-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="87083-105">`QueryId`Метод получает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="87083-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="87083-106">Этот метод реализует метод [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="87083-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="87083-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87083-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="87083-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="87083-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87083-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="87083-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="87083-110">Получает строку, содержащую идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="87083-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87083-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87083-111">Return value</span></span>

<span data-ttu-id="87083-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="87083-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="87083-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="87083-113">Return code</span></span>                                                                                   | <span data-ttu-id="87083-114">Описание</span><span class="sxs-lookup"><span data-stu-id="87083-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="87083-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="87083-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="87083-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="87083-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="87083-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="87083-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="87083-118">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="87083-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="87083-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="87083-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="87083-120">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="87083-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87083-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87083-121">Remarks</span></span>

<span data-ttu-id="87083-122">Идентификатор ПИН-кода используется для сохраняемости графа.</span><span class="sxs-lookup"><span data-stu-id="87083-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="87083-123">Идентификатор ПИН-кода для этого класса находится в.</span><span class="sxs-lookup"><span data-stu-id="87083-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="87083-124">Этот класс переопределяет поведение класса [**кбасепин**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="87083-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="87083-125">В классе **кбасепин** идентификатор ПИН-кода совпадает с именем ПИН-кода, указанным в конструкторе класса.</span><span class="sxs-lookup"><span data-stu-id="87083-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="87083-126">В классе **ктрансформинпутпин** идентификатор ПИН-кода и имя ПИН-кода не совпадают.</span><span class="sxs-lookup"><span data-stu-id="87083-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="87083-127">Требования</span><span class="sxs-lookup"><span data-stu-id="87083-127">Requirements</span></span>



| <span data-ttu-id="87083-128">Требование</span><span class="sxs-lookup"><span data-stu-id="87083-128">Requirement</span></span> | <span data-ttu-id="87083-129">Значение</span><span class="sxs-lookup"><span data-stu-id="87083-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87083-130">Header</span><span class="sxs-lookup"><span data-stu-id="87083-130">Header</span></span><br/>  | <dl> <span data-ttu-id="87083-131"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87083-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87083-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87083-132">Library</span></span><br/> | <dl> <span data-ttu-id="87083-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="87083-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




