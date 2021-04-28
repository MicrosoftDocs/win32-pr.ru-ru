---
description: MFPKEY_RESIZE_INTERLACE свойство — указывает, является ли входной поток чередованием.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Свойство MFPKEY_RESIZE_INTERLACE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092882"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="2e3ad-103">МФПКЭЙ \_ \_ Свойства развертки изменения размера</span><span class="sxs-lookup"><span data-stu-id="2e3ad-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="2e3ad-104">Указывает, является ли входной поток чередованием.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2e3ad-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="2e3ad-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2e3ad-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2e3ad-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2e3ad-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2e3ad-107">Data Type</span></span>

<span data-ttu-id="2e3ad-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="2e3ad-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="2e3ad-109">Применение</span><span class="sxs-lookup"><span data-stu-id="2e3ad-109">Applies To</span></span>

-   [<span data-ttu-id="2e3ad-110">DSP изменения видеоконтроллеров</span><span class="sxs-lookup"><span data-stu-id="2e3ad-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="2e3ad-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="2e3ad-111">Remarks</span></span>

<span data-ttu-id="2e3ad-112">Используйте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2e3ad-112">Use one of the following values:</span></span>



| <span data-ttu-id="2e3ad-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3ad-113">Value</span></span>     | <span data-ttu-id="2e3ad-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2e3ad-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="2e3ad-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="2e3ad-115">VT\_FALSE</span></span> | <span data-ttu-id="2e3ad-116">прогрессивный</span><span class="sxs-lookup"><span data-stu-id="2e3ad-116">Progressive</span></span> |
| <span data-ttu-id="2e3ad-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="2e3ad-117">VT\_TRUE</span></span>  | <span data-ttu-id="2e3ad-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="2e3ad-118">Interlaced</span></span>  |



 

<span data-ttu-id="2e3ad-119">Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="2e3ad-120">Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3ad-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2e3ad-121">Requirements</span></span>



| <span data-ttu-id="2e3ad-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2e3ad-122">Requirement</span></span> | <span data-ttu-id="2e3ad-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3ad-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ad-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e3ad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3ad-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e3ad-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e3ad-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e3ad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3ad-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e3ad-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e3ad-128">Header</span><span class="sxs-lookup"><span data-stu-id="2e3ad-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e3ad-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ad-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e3ad-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2e3ad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e3ad-131">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e3ad-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
