---
description: Указывает, является ли входной поток чередованием.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Свойство MFPKEY_COLORCONV_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812772"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="23bae-103">МФПКЭЙ \_ колорконв \_ mode, свойство</span><span class="sxs-lookup"><span data-stu-id="23bae-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="23bae-104">Указывает, является ли входной поток чередованием.</span><span class="sxs-lookup"><span data-stu-id="23bae-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="23bae-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="23bae-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="23bae-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="23bae-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="23bae-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="23bae-107">Data Type</span></span>

<span data-ttu-id="23bae-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="23bae-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="23bae-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="23bae-109">Default Value</span></span>

<span data-ttu-id="23bae-110">Вычислено DSP из исходного видео.</span><span class="sxs-lookup"><span data-stu-id="23bae-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="23bae-111">Применение</span><span class="sxs-lookup"><span data-stu-id="23bae-111">Applies To</span></span>

-   [<span data-ttu-id="23bae-112">DSP цветового преобразователя</span><span class="sxs-lookup"><span data-stu-id="23bae-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="23bae-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23bae-113">Remarks</span></span>

<span data-ttu-id="23bae-114">Используйте одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="23bae-114">Use one of the following values.</span></span>



| <span data-ttu-id="23bae-115">Значение</span><span class="sxs-lookup"><span data-stu-id="23bae-115">Value</span></span> | <span data-ttu-id="23bae-116">Описание</span><span class="sxs-lookup"><span data-stu-id="23bae-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="23bae-117">0</span><span class="sxs-lookup"><span data-stu-id="23bae-117">0</span></span>     | <span data-ttu-id="23bae-118">прогрессивный</span><span class="sxs-lookup"><span data-stu-id="23bae-118">Progressive</span></span> |
| <span data-ttu-id="23bae-119">2</span><span class="sxs-lookup"><span data-stu-id="23bae-119">2</span></span>     | <span data-ttu-id="23bae-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="23bae-120">Interlaced</span></span>  |



 

<span data-ttu-id="23bae-121">Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием.</span><span class="sxs-lookup"><span data-stu-id="23bae-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="23bae-122">Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="23bae-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="23bae-123">Требования</span><span class="sxs-lookup"><span data-stu-id="23bae-123">Requirements</span></span>



| <span data-ttu-id="23bae-124">Требование</span><span class="sxs-lookup"><span data-stu-id="23bae-124">Requirement</span></span> | <span data-ttu-id="23bae-125">Значение</span><span class="sxs-lookup"><span data-stu-id="23bae-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23bae-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23bae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="23bae-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="23bae-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="23bae-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23bae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="23bae-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23bae-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23bae-130">Header</span><span class="sxs-lookup"><span data-stu-id="23bae-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="23bae-131"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="23bae-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23bae-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23bae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23bae-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23bae-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
