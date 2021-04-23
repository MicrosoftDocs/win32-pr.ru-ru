---
description: 'Метод Properties извлекает свойства образца. Этот метод реализует метод IMediaSample2:: Properties.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Метод Кмедиасампле.-Properties (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665218"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="05692-104">Кмедиасампле... Properties, метод</span><span class="sxs-lookup"><span data-stu-id="05692-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="05692-105">`GetProperties`Метод получает свойства образца.</span><span class="sxs-lookup"><span data-stu-id="05692-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="05692-106">Этот метод реализует метод [**IMediaSample2:: Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="05692-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05692-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05692-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="05692-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05692-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05692-109">*кбпропертиес*</span><span class="sxs-lookup"><span data-stu-id="05692-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="05692-110">Длина извлекаемых данных свойства в байтах.</span><span class="sxs-lookup"><span data-stu-id="05692-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="05692-111">*пбпропертиес*</span><span class="sxs-lookup"><span data-stu-id="05692-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="05692-112">Указатель на буфер размера *кбпропертиес*.</span><span class="sxs-lookup"><span data-stu-id="05692-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05692-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05692-113">Return value</span></span>

<span data-ttu-id="05692-114">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="05692-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="05692-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="05692-115">Return code</span></span>                                                                               | <span data-ttu-id="05692-116">Описание</span><span class="sxs-lookup"><span data-stu-id="05692-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="05692-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="05692-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="05692-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="05692-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="05692-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="05692-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="05692-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="05692-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05692-121">Требования</span><span class="sxs-lookup"><span data-stu-id="05692-121">Requirements</span></span>



| <span data-ttu-id="05692-122">Требование</span><span class="sxs-lookup"><span data-stu-id="05692-122">Requirement</span></span> | <span data-ttu-id="05692-123">Значение</span><span class="sxs-lookup"><span data-stu-id="05692-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05692-124">Header</span><span class="sxs-lookup"><span data-stu-id="05692-124">Header</span></span><br/>  | <dl> <span data-ttu-id="05692-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05692-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05692-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05692-126">Library</span></span><br/> | <dl> <span data-ttu-id="05692-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="05692-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05692-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05692-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05692-129">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="05692-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




