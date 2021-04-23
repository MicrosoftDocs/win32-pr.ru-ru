---
description: Метод QueryId извлекает идентификатор для ПИН-кода.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Метод Ксаурцестреам. QueryId (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676002"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="97b55-103">Ксаурцестреам. QueryId, метод</span><span class="sxs-lookup"><span data-stu-id="97b55-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="97b55-104">`QueryId`Метод получает идентификатор для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="97b55-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97b55-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="97b55-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97b55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b55-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="97b55-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="97b55-108">Указатель на переменную, которая получает строку, содержащую идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="97b55-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97b55-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97b55-109">Return value</span></span>

<span data-ttu-id="97b55-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="97b55-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="97b55-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="97b55-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="97b55-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="97b55-112">Return code</span></span>                                                                                       | <span data-ttu-id="97b55-113">Описание</span><span class="sxs-lookup"><span data-stu-id="97b55-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="97b55-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="97b55-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="97b55-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="97b55-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="97b55-116"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="97b55-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="97b55-117">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="97b55-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="97b55-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="97b55-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="97b55-119">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="97b55-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="97b55-120"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="97b55-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="97b55-121">ПИН-код не найден в фильтре.</span><span class="sxs-lookup"><span data-stu-id="97b55-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97b55-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97b55-122">Remarks</span></span>

<span data-ttu-id="97b55-123">Этот метод реализует метод [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="97b55-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="97b55-124">Чтобы создать строку идентификатора, ПИН-код вызывает метод [**ксаурце:: финдпиннумбер**](csource-findpinnumber.md) с самим собой в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="97b55-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="97b55-125">Метод **финдпиннумбер** возвращает PIN-код, индексируемый от нуля.</span><span class="sxs-lookup"><span data-stu-id="97b55-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="97b55-126">`QueryId` увеличивает возвращаемое значение на единицу и преобразует результат в строку.</span><span class="sxs-lookup"><span data-stu-id="97b55-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="97b55-127">Например, первый ПИН-код принимает значение 1. второй ПИН-код преобразуется в «2»; и т. д.</span><span class="sxs-lookup"><span data-stu-id="97b55-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="97b55-128">Если этот метод возвращает VFW \_ E \_ не \_ найден, это означает, что массив ПИН-кодов фильтра является недопустимым, предположительно вызвано ошибкой в фильтре.</span><span class="sxs-lookup"><span data-stu-id="97b55-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b55-129">Требования</span><span class="sxs-lookup"><span data-stu-id="97b55-129">Requirements</span></span>



| <span data-ttu-id="97b55-130">Требование</span><span class="sxs-lookup"><span data-stu-id="97b55-130">Requirement</span></span> | <span data-ttu-id="97b55-131">Значение</span><span class="sxs-lookup"><span data-stu-id="97b55-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b55-132">Header</span><span class="sxs-lookup"><span data-stu-id="97b55-132">Header</span></span><br/>  | <dl> <span data-ttu-id="97b55-133"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97b55-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="97b55-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97b55-134">Library</span></span><br/> | <dl> <span data-ttu-id="97b55-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="97b55-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b55-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97b55-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b55-137">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="97b55-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




