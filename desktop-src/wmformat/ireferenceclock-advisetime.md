---
title: Иреференцеклокк Адвисетиме, метод
description: Метод Адвисетиме запрашивает асинхронное уведомление о том, что прошло время.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Формат Windows Media, Адвисетиме метод
- Адвисетиме метод Windows Media Format, интерфейс Иреференцеклокк
- Интерфейс Иреференцеклокк Windows Media Format, метод Адвисетиме
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105719071"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="4ed5a-106">Метод Иреференцеклокк:: Адвисетиме</span><span class="sxs-lookup"><span data-stu-id="4ed5a-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="4ed5a-107">Метод **адвисетиме** запрашивает асинхронное уведомление о том, что прошло время.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed5a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ed5a-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="4ed5a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ed5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ed5a-110">*ртбасетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ed5a-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed5a-111">Базовое время ссылки в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4ed5a-112">*ртстреамтиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ed5a-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed5a-113">Время смещения потока (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="4ed5a-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4ed5a-114">*Хевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ed5a-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed5a-115">Обработчик события, созданный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="4ed5a-116">Это событие будет сигнальным по истечении указанного времени.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="4ed5a-117">*пдвадвисекукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ed5a-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ed5a-118">Указатель на переменную, которая получает идентификатор для запроса.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="4ed5a-119">Он используется для обнаружения этого вызова в **адвисетиме** в будущем, например для отмены запроса.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ed5a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ed5a-120">Return value</span></span>

<span data-ttu-id="4ed5a-121">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4ed5a-122">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4ed5a-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4ed5a-123">Return code</span></span>                                                                               | <span data-ttu-id="4ed5a-124">Описание</span><span class="sxs-lookup"><span data-stu-id="4ed5a-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="4ed5a-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed5a-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4ed5a-126">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="4ed5a-127"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed5a-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4ed5a-128">Параметр *пдвадвисекукие* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="4ed5a-129"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed5a-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="4ed5a-130">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="4ed5a-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="4ed5a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ed5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed5a-132">**Интерфейс Иреференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="4ed5a-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





