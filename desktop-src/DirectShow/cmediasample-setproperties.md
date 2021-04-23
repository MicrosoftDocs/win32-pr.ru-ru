---
description: 'Метод SetProperties задает свойства образца. Этот метод реализует метод IMediaSample2:: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Кмедиасампле. SetProperties, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674905"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="c2999-104">Кмедиасампле. SetProperties, метод</span><span class="sxs-lookup"><span data-stu-id="c2999-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="c2999-105">`SetProperties`Метод задает свойства образца.</span><span class="sxs-lookup"><span data-stu-id="c2999-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="c2999-106">Этот метод реализует метод [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="c2999-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2999-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2999-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="c2999-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2999-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2999-109">*кбпропертиес*</span><span class="sxs-lookup"><span data-stu-id="c2999-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="c2999-110">Длина устанавливаемых данных свойств в байтах.</span><span class="sxs-lookup"><span data-stu-id="c2999-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c2999-111">*пбпропертиес*</span><span class="sxs-lookup"><span data-stu-id="c2999-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="c2999-112">Указатель на буфер размера *кбпропертиес*.</span><span class="sxs-lookup"><span data-stu-id="c2999-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2999-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2999-113">Return value</span></span>

<span data-ttu-id="c2999-114">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c2999-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c2999-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c2999-115">Return code</span></span>                                                                                   | <span data-ttu-id="c2999-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c2999-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="c2999-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c2999-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c2999-118">Успешно</span><span class="sxs-lookup"><span data-stu-id="c2999-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="c2999-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c2999-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c2999-120">Недопустимый аргумент</span><span class="sxs-lookup"><span data-stu-id="c2999-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="c2999-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c2999-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c2999-122">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="c2999-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="c2999-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c2999-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c2999-124">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="c2999-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c2999-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c2999-125">Requirements</span></span>



| <span data-ttu-id="c2999-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c2999-126">Requirement</span></span> | <span data-ttu-id="c2999-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c2999-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2999-128">Header</span><span class="sxs-lookup"><span data-stu-id="c2999-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c2999-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2999-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2999-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2999-130">Library</span></span><br/> | <dl> <span data-ttu-id="c2999-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c2999-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2999-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2999-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2999-133">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="c2999-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




