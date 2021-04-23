---
description: 'Метод Исформатсуппортед определяет, поддерживается ли указанный формат времени. Этот метод реализует метод Имедиасикинг:: Исформатсуппортед.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Кпоспасссру. Исформатсуппортед, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679965"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="3a394-104">Кпоспасссру. Исформатсуппортед, метод</span><span class="sxs-lookup"><span data-stu-id="3a394-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="3a394-105">`IsFormatSupported`Метод определяет, поддерживается ли указанный формат времени.</span><span class="sxs-lookup"><span data-stu-id="3a394-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="3a394-106">Этот метод реализует метод [**имедиасикинг:: исформатсуппортед**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="3a394-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a394-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a394-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3a394-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a394-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="3a394-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3a394-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="3a394-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a394-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a394-111">Return value</span></span>

<span data-ttu-id="3a394-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="3a394-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a394-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3a394-113">Requirements</span></span>



| <span data-ttu-id="3a394-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3a394-114">Requirement</span></span> | <span data-ttu-id="3a394-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3a394-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a394-116">Header</span><span class="sxs-lookup"><span data-stu-id="3a394-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3a394-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a394-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a394-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3a394-118">Library</span></span><br/> | <dl> <span data-ttu-id="3a394-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3a394-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a394-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a394-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a394-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="3a394-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="3a394-122">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="3a394-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




