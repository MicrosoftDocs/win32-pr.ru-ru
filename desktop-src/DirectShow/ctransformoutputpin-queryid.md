---
description: 'Ктрансформаутпутпин. QueryId, метод QueryId извлекает идентификатор для ПИН-кода. Этот метод реализует метод Ипин:: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Ктрансформаутпутпин. QueryId, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094852"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="1cddb-104">Ктрансформаутпутпин. QueryId, метод</span><span class="sxs-lookup"><span data-stu-id="1cddb-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="1cddb-105">`QueryId`Метод получает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="1cddb-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="1cddb-106">Этот метод реализует метод [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="1cddb-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cddb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cddb-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="1cddb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cddb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cddb-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="1cddb-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="1cddb-110">Получает строку, содержащую идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="1cddb-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cddb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cddb-111">Return value</span></span>

<span data-ttu-id="1cddb-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1cddb-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1cddb-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1cddb-113">Return code</span></span>                                                                                   | <span data-ttu-id="1cddb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1cddb-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="1cddb-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1cddb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1cddb-116">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="1cddb-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="1cddb-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1cddb-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1cddb-118">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="1cddb-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="1cddb-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1cddb-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1cddb-120">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="1cddb-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1cddb-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="1cddb-121">Remarks</span></span>

<span data-ttu-id="1cddb-122">Идентификатор ПИН-кода используется для сохраняемости графа.</span><span class="sxs-lookup"><span data-stu-id="1cddb-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="1cddb-123">Идентификатор ПИН-кода для этого класса истекает. Этот класс переопределяет поведение класса [**кбасепин**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="1cddb-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="1cddb-124">В классе **кбасепин** идентификатор ПИН-кода совпадает с именем ПИН-кода, указанным в конструкторе класса.</span><span class="sxs-lookup"><span data-stu-id="1cddb-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="1cddb-125">В классе **ктрансформинпутпин** идентификатор ПИН-кода и имя ПИН-кода не совпадают.</span><span class="sxs-lookup"><span data-stu-id="1cddb-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cddb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1cddb-126">Requirements</span></span>



| <span data-ttu-id="1cddb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="1cddb-127">Requirement</span></span> | <span data-ttu-id="1cddb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1cddb-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cddb-129">Header</span><span class="sxs-lookup"><span data-stu-id="1cddb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1cddb-130"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cddb-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1cddb-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1cddb-131">Library</span></span><br/> | <dl> <span data-ttu-id="1cddb-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1cddb-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




