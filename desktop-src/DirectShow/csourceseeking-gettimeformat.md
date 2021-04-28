---
description: 'Ксаурцесикинг. Жеттимеформат, метод Жеттимеформат извлекает текущий формат времени. Этот метод реализует метод Имедиасикинг:: Жеттимеформат.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Ксаурцесикинг. Жеттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085222"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="5def9-104">Ксаурцесикинг. Жеттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="5def9-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="5def9-105">`GetTimeFormat`Метод получает текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="5def9-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="5def9-106">Этот метод реализует метод [**имедиасикинг:: жеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="5def9-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5def9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5def9-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="5def9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5def9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5def9-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="5def9-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="5def9-110">Указатель на переменную, которая получает GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="5def9-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="5def9-111">См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="5def9-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5def9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5def9-112">Return value</span></span>

<span data-ttu-id="5def9-113">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5def9-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="5def9-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5def9-114">Return code</span></span>                                                                               | <span data-ttu-id="5def9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5def9-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="5def9-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5def9-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5def9-117">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="5def9-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="5def9-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5def9-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5def9-119">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="5def9-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5def9-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="5def9-120">Remarks</span></span>

<span data-ttu-id="5def9-121">Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).</span><span class="sxs-lookup"><span data-stu-id="5def9-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="5def9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5def9-122">Requirements</span></span>



| <span data-ttu-id="5def9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5def9-123">Requirement</span></span> | <span data-ttu-id="5def9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5def9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5def9-125">Header</span><span class="sxs-lookup"><span data-stu-id="5def9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5def9-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5def9-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5def9-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5def9-127">Library</span></span><br/> | <dl> <span data-ttu-id="5def9-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5def9-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5def9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5def9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5def9-130">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="5def9-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




