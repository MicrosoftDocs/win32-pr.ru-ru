---
description: 'Метод capabilities извлекает все возможности поиска в потоке. Этот метод реализует метод Имедиасикинг:: Capabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Метод Кпоспасссру. Capabilities (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657228"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="31164-104">Кпоспасссру. capabilities, метод</span><span class="sxs-lookup"><span data-stu-id="31164-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="31164-105">Метод **capabilities** извлекает все возможности поиска в потоке.</span><span class="sxs-lookup"><span data-stu-id="31164-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="31164-106">Этот метод реализует метод [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="31164-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="31164-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31164-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="31164-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="31164-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31164-109">*пкапабилитиес*</span><span class="sxs-lookup"><span data-stu-id="31164-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="31164-110">Указатель на переменную, которая получает побитовую комбинацию флагов [**\_ \_ поиска \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="31164-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31164-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31164-111">Return value</span></span>

<span data-ttu-id="31164-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="31164-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="31164-113">Требования</span><span class="sxs-lookup"><span data-stu-id="31164-113">Requirements</span></span>



| <span data-ttu-id="31164-114">Требование</span><span class="sxs-lookup"><span data-stu-id="31164-114">Requirement</span></span> | <span data-ttu-id="31164-115">Значение</span><span class="sxs-lookup"><span data-stu-id="31164-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31164-116">Header</span><span class="sxs-lookup"><span data-stu-id="31164-116">Header</span></span><br/>  | <dl> <span data-ttu-id="31164-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31164-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31164-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31164-118">Library</span></span><br/> | <dl> <span data-ttu-id="31164-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="31164-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31164-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31164-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31164-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="31164-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




