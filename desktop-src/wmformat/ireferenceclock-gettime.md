---
title: Иреференцеклокк метода времени
description: Метод Time извлекает текущее время ссылки.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Метод Time формат Windows Media
- Метод Time формат Windows Media, интерфейс Иреференцеклокк
- Интерфейс Иреференцеклокк интерфейса Windows Media Format, метод
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411985"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="68edc-106">Метод Иреференцеклокк:: OnTime</span><span class="sxs-lookup"><span data-stu-id="68edc-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="68edc-107">Метод **time** извлекает текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="68edc-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="68edc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68edc-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="68edc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="68edc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68edc-110">*птиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68edc-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68edc-111">Указатель на переменную, которая получает текущее время в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="68edc-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68edc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68edc-112">Return value</span></span>

<span data-ttu-id="68edc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="68edc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="68edc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="68edc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="68edc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="68edc-115">Return code</span></span>                                                                               | <span data-ttu-id="68edc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="68edc-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="68edc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="68edc-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="68edc-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="68edc-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="68edc-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="68edc-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="68edc-120">Параметр *птиме* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="68edc-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="68edc-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68edc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68edc-122">**Интерфейс Иреференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="68edc-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





