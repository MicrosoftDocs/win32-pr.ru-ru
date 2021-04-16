---
description: 'Метод Get \_ CurrentPosition извлекает текущую координату относительно общей продолжительности потока. Этот метод реализует метод Имедиапоситион:: Get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Метод CPosPassThru.get_CurrentPosition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657213"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="4562c-104">Кпоспасссру. Get \_ CurrentPosition, метод</span><span class="sxs-lookup"><span data-stu-id="4562c-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="4562c-105">`get_CurrentPosition`Метод получает текущую координату относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="4562c-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="4562c-106">Этот метод реализует метод [**имедиапоситион:: Get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="4562c-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4562c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4562c-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="4562c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4562c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4562c-109">*пллтиме*</span><span class="sxs-lookup"><span data-stu-id="4562c-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="4562c-110">Указатель на переменную, которая получает текущую точку в секундах.</span><span class="sxs-lookup"><span data-stu-id="4562c-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4562c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4562c-111">Return value</span></span>

<span data-ttu-id="4562c-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4562c-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4562c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4562c-113">Requirements</span></span>



| <span data-ttu-id="4562c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4562c-114">Requirement</span></span> | <span data-ttu-id="4562c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4562c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4562c-116">Header</span><span class="sxs-lookup"><span data-stu-id="4562c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4562c-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4562c-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4562c-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4562c-118">Library</span></span><br/> | <dl> <span data-ttu-id="4562c-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4562c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4562c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4562c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4562c-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="4562c-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




