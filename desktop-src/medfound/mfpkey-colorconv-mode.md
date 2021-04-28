---
description: MFPKEY_COLORCONV_MODE свойство — указывает, является ли входной поток чередованием.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Свойство MFPKEY_COLORCONV_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087582"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="59bf8-103">МФПКЭЙ \_ колорконв \_ mode, свойство</span><span class="sxs-lookup"><span data-stu-id="59bf8-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="59bf8-104">Указывает, является ли входной поток чередованием.</span><span class="sxs-lookup"><span data-stu-id="59bf8-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="59bf8-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="59bf8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="59bf8-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="59bf8-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="59bf8-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="59bf8-107">Data Type</span></span>

<span data-ttu-id="59bf8-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="59bf8-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="59bf8-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="59bf8-109">Default Value</span></span>

<span data-ttu-id="59bf8-110">Вычислено DSP из исходного видео.</span><span class="sxs-lookup"><span data-stu-id="59bf8-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="59bf8-111">Применение</span><span class="sxs-lookup"><span data-stu-id="59bf8-111">Applies To</span></span>

-   [<span data-ttu-id="59bf8-112">DSP цветового преобразователя</span><span class="sxs-lookup"><span data-stu-id="59bf8-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="59bf8-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="59bf8-113">Remarks</span></span>

<span data-ttu-id="59bf8-114">Используйте одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="59bf8-114">Use one of the following values.</span></span>



| <span data-ttu-id="59bf8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="59bf8-115">Value</span></span> | <span data-ttu-id="59bf8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="59bf8-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="59bf8-117">0</span><span class="sxs-lookup"><span data-stu-id="59bf8-117">0</span></span>     | <span data-ttu-id="59bf8-118">прогрессивный</span><span class="sxs-lookup"><span data-stu-id="59bf8-118">Progressive</span></span> |
| <span data-ttu-id="59bf8-119">2</span><span class="sxs-lookup"><span data-stu-id="59bf8-119">2</span></span>     | <span data-ttu-id="59bf8-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="59bf8-120">Interlaced</span></span>  |



 

<span data-ttu-id="59bf8-121">Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием.</span><span class="sxs-lookup"><span data-stu-id="59bf8-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="59bf8-122">Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59bf8-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="59bf8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="59bf8-123">Requirements</span></span>



| <span data-ttu-id="59bf8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="59bf8-124">Requirement</span></span> | <span data-ttu-id="59bf8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="59bf8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59bf8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59bf8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="59bf8-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="59bf8-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="59bf8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59bf8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="59bf8-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59bf8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59bf8-130">Header</span><span class="sxs-lookup"><span data-stu-id="59bf8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="59bf8-131"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="59bf8-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59bf8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="59bf8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bf8-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59bf8-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
