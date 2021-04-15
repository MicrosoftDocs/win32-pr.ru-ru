---
description: 'Метод Чекккапабилитиес запрашивает, есть ли у потока указанные возможности поиска. Этот метод реализует метод Имедиасикинг:: Чекккапабилитиес.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Кпоспасссру. Чекккапабилитиес, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675787"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="6ceda-104">Кпоспасссру. Чекккапабилитиес, метод</span><span class="sxs-lookup"><span data-stu-id="6ceda-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="6ceda-105">`CheckCapabilities`Метод запрашивает, имеет ли поток указанные возможности поиска.</span><span class="sxs-lookup"><span data-stu-id="6ceda-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="6ceda-106">Этот метод реализует метод [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="6ceda-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ceda-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ceda-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="6ceda-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ceda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ceda-109">*пкапабилитиес*</span><span class="sxs-lookup"><span data-stu-id="6ceda-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="6ceda-110">Указатель на побитовую комбинацию одного или нескольких атрибутов [**\_ \_ \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) поиска.</span><span class="sxs-lookup"><span data-stu-id="6ceda-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="6ceda-111">При возврате из метода значение указывает, какие из этих атрибутов доступны.</span><span class="sxs-lookup"><span data-stu-id="6ceda-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ceda-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-112">Return value</span></span>

<span data-ttu-id="6ceda-113">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="6ceda-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ceda-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6ceda-114">Requirements</span></span>



| <span data-ttu-id="6ceda-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6ceda-115">Requirement</span></span> | <span data-ttu-id="6ceda-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6ceda-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ceda-117">Header</span><span class="sxs-lookup"><span data-stu-id="6ceda-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6ceda-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ceda-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ceda-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ceda-119">Library</span></span><br/> | <dl> <span data-ttu-id="6ceda-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6ceda-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ceda-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ceda-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ceda-122">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="6ceda-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




