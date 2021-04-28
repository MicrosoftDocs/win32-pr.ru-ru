---
description: 'Кпоспасссру. Исформатсуппортед, метод Исформатсуппортед определяет, поддерживается ли указанный формат времени. Этот метод реализует метод Имедиасикинг:: Исформатсуппортед.'
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
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095252"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="2c924-104">Кпоспасссру. Исформатсуппортед, метод</span><span class="sxs-lookup"><span data-stu-id="2c924-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="2c924-105">`IsFormatSupported`Метод определяет, поддерживается ли указанный формат времени.</span><span class="sxs-lookup"><span data-stu-id="2c924-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="2c924-106">Этот метод реализует метод [**имедиасикинг:: исформатсуппортед**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="2c924-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c924-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c924-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2c924-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c924-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c924-109">*пформат*</span><span class="sxs-lookup"><span data-stu-id="2c924-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2c924-110">Указатель на GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="2c924-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c924-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c924-111">Return value</span></span>

<span data-ttu-id="2c924-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="2c924-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c924-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2c924-113">Requirements</span></span>



| <span data-ttu-id="2c924-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2c924-114">Requirement</span></span> | <span data-ttu-id="2c924-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2c924-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c924-116">Header</span><span class="sxs-lookup"><span data-stu-id="2c924-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2c924-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c924-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c924-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c924-118">Library</span></span><br/> | <dl> <span data-ttu-id="2c924-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2c924-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c924-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2c924-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c924-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="2c924-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="2c924-122">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="2c924-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




