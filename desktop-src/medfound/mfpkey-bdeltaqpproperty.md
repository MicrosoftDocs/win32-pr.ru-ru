---
description: Указывает Дельта-увеличение между рисунком куантизер фрейма привязки и изображением куантизер в B-кадре.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Свойство MFPKEY_BDELTAQP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693048"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="49cf8-103">МФПКЭЙ \_ бделтакп, свойство</span><span class="sxs-lookup"><span data-stu-id="49cf8-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="49cf8-104">Указывает Дельта-увеличение между рисунком куантизер фрейма привязки и изображением куантизер в B-кадре.</span><span class="sxs-lookup"><span data-stu-id="49cf8-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="49cf8-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="49cf8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="49cf8-106">g \_ всзвмвкбделтакп</span><span class="sxs-lookup"><span data-stu-id="49cf8-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="49cf8-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="49cf8-107">Data Type</span></span>

<span data-ttu-id="49cf8-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="49cf8-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="49cf8-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="49cf8-109">Default Value</span></span>

<span data-ttu-id="49cf8-110">0</span><span class="sxs-lookup"><span data-stu-id="49cf8-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="49cf8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49cf8-111">Remarks</span></span>

<span data-ttu-id="49cf8-112">Picture куантизер (QP) — это мера сжатия кадра.</span><span class="sxs-lookup"><span data-stu-id="49cf8-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="49cf8-113">Более высокие значения представляют более высокие коэффициенты сжатия.</span><span class="sxs-lookup"><span data-stu-id="49cf8-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="49cf8-114">QP можно задать с шагом в половину точек.</span><span class="sxs-lookup"><span data-stu-id="49cf8-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="49cf8-115">Как правило, B-кадр сжимается в обработчике запросов так же, как или 0,5 выше, чем обработчик QP маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="49cf8-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="49cf8-116">При указании разностного пакета запросов в виде «B-Frame» выше 0 можно сжимать B-кадры при увеличении коэффициента сжатия.</span><span class="sxs-lookup"><span data-stu-id="49cf8-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="49cf8-117">Разностный обработчик запросов "B-Frame" можно задать только в приращениях с целыми точками.</span><span class="sxs-lookup"><span data-stu-id="49cf8-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="49cf8-118">Этому свойству должно быть присвоено целое значение от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="49cf8-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="49cf8-119">Рекомендуемое значение — 1.</span><span class="sxs-lookup"><span data-stu-id="49cf8-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cf8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="49cf8-120">Requirements</span></span>



| <span data-ttu-id="49cf8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="49cf8-121">Requirement</span></span> | <span data-ttu-id="49cf8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="49cf8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49cf8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49cf8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="49cf8-124">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="49cf8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49cf8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="49cf8-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49cf8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49cf8-127">Header</span><span class="sxs-lookup"><span data-stu-id="49cf8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cf8-128"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cf8-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cf8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49cf8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cf8-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="49cf8-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




