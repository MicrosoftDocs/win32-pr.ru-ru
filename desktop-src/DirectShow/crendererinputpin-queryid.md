---
description: 'Метод QueryId извлекает идентификатор ПИН-кода. Этот метод переопределяет метод Кбасепин:: QueryId.'
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Крендереринпутпин. QueryId, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669371"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="9378c-104">Крендереринпутпин. QueryId, метод</span><span class="sxs-lookup"><span data-stu-id="9378c-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="9378c-105">`QueryId`Метод получает идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9378c-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="9378c-106">Этот метод переопределяет метод [**кбасепин:: QueryId**](cbasepin-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="9378c-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9378c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9378c-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="9378c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9378c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9378c-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="9378c-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="9378c-110">Получает строку, содержащую идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9378c-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9378c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9378c-111">Return value</span></span>

<span data-ttu-id="9378c-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9378c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9378c-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9378c-113">Return code</span></span>                                                                                   | <span data-ttu-id="9378c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9378c-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="9378c-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9378c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9378c-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="9378c-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="9378c-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9378c-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9378c-118">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="9378c-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="9378c-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9378c-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9378c-120">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="9378c-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9378c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9378c-121">Remarks</span></span>

<span data-ttu-id="9378c-122">Этот метод выделяет строку расширенных символов "in" и присваивает ее параметру *ID* .</span><span class="sxs-lookup"><span data-stu-id="9378c-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="9378c-123">Вызывающий объект должен освободить выделенную память с помощью функции **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="9378c-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9378c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9378c-124">Requirements</span></span>



| <span data-ttu-id="9378c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9378c-125">Requirement</span></span> | <span data-ttu-id="9378c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9378c-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9378c-127">Header</span><span class="sxs-lookup"><span data-stu-id="9378c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9378c-128"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9378c-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9378c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9378c-129">Library</span></span><br/> | <dl> <span data-ttu-id="9378c-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9378c-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9378c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9378c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9378c-132">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="9378c-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




