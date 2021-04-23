---
title: Метод Ивмдрмлиценсе Жетаналогвидеорестриктионлевелс (Вмдрмсдк. h)
description: Метод Жетаналогвидеорестриктионлевелс извлекает все аналоговые видеоограничения, установленные для текущей лицензии.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Формат Windows Media, Жетаналогвидеорестриктионлевелс метод
- Жетаналогвидеорестриктионлевелс метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Жетаналогвидеорестриктионлевелс
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704475"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="f1751-106">Метод Ивмдрмлиценсе:: Жетаналогвидеорестриктионлевелс</span><span class="sxs-lookup"><span data-stu-id="f1751-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="f1751-107">Метод **жетаналогвидеорестриктионлевелс** извлекает все аналоговые видеоограничения, установленные для текущей лицензии.</span><span class="sxs-lookup"><span data-stu-id="f1751-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1751-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1751-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="f1751-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1751-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1751-110">*\[ рганалогвидеорестриктионс \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="f1751-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1751-111">Получает массив структур [**\_ ограничений аналогового \_ видео \_ WMDRM**](wmdrm-analog-video-restrictions.md) .</span><span class="sxs-lookup"><span data-stu-id="f1751-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="f1751-112">Задайте значение **null** , чтобы получить количество элементов в массиве в *пкресктриктионс*.</span><span class="sxs-lookup"><span data-stu-id="f1751-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="f1751-113">*пкрестриктионс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f1751-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1751-114">Число элементов в массиве ограничений.</span><span class="sxs-lookup"><span data-stu-id="f1751-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="f1751-115">Если *рганалогвидеорестриктионс* имеет значение **null**, для этого параметра задается количество элементов, необходимых в массиве.</span><span class="sxs-lookup"><span data-stu-id="f1751-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1751-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1751-116">Return value</span></span>

<span data-ttu-id="f1751-117">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f1751-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f1751-118">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f1751-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f1751-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f1751-119">Return code</span></span>                                                                          | <span data-ttu-id="f1751-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f1751-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f1751-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f1751-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f1751-122">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f1751-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1751-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1751-123">Remarks</span></span>

<span data-ttu-id="f1751-124">Необходимо выделить память для массива ограничений.</span><span class="sxs-lookup"><span data-stu-id="f1751-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="f1751-125">Чтобы сделать это, сначала вызовите метод с параметром *рганалогвидеорестриктионс* , которому присвоено значение **null**, которое задаст в параметре *пкрестриктионс* число обязательных элементов.</span><span class="sxs-lookup"><span data-stu-id="f1751-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1751-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f1751-126">Requirements</span></span>



| <span data-ttu-id="f1751-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f1751-127">Requirement</span></span> | <span data-ttu-id="f1751-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f1751-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1751-129">Header</span><span class="sxs-lookup"><span data-stu-id="f1751-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f1751-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1751-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1751-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1751-131">Library</span></span><br/> | <dl> <span data-ttu-id="f1751-132"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1751-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1751-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1751-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1751-134">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="f1751-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





