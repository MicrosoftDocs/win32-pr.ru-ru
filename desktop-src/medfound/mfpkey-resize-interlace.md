---
description: Указывает, является ли входной поток чередованием.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Свойство MFPKEY_RESIZE_INTERLACE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662827"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="24f8f-103">МФПКЭЙ \_ \_ Свойства развертки изменения размера</span><span class="sxs-lookup"><span data-stu-id="24f8f-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="24f8f-104">Указывает, является ли входной поток чередованием.</span><span class="sxs-lookup"><span data-stu-id="24f8f-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="24f8f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="24f8f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="24f8f-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="24f8f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="24f8f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="24f8f-107">Data Type</span></span>

<span data-ttu-id="24f8f-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="24f8f-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="24f8f-109">Применение</span><span class="sxs-lookup"><span data-stu-id="24f8f-109">Applies To</span></span>

-   [<span data-ttu-id="24f8f-110">DSP изменения видеоконтроллеров</span><span class="sxs-lookup"><span data-stu-id="24f8f-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="24f8f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24f8f-111">Remarks</span></span>

<span data-ttu-id="24f8f-112">Используйте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="24f8f-112">Use one of the following values:</span></span>



| <span data-ttu-id="24f8f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="24f8f-113">Value</span></span>     | <span data-ttu-id="24f8f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="24f8f-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="24f8f-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="24f8f-115">VT\_FALSE</span></span> | <span data-ttu-id="24f8f-116">прогрессивный</span><span class="sxs-lookup"><span data-stu-id="24f8f-116">Progressive</span></span> |
| <span data-ttu-id="24f8f-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="24f8f-117">VT\_TRUE</span></span>  | <span data-ttu-id="24f8f-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="24f8f-118">Interlaced</span></span>  |



 

<span data-ttu-id="24f8f-119">Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием.</span><span class="sxs-lookup"><span data-stu-id="24f8f-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="24f8f-120">Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="24f8f-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f8f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="24f8f-121">Requirements</span></span>



| <span data-ttu-id="24f8f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="24f8f-122">Requirement</span></span> | <span data-ttu-id="24f8f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="24f8f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f8f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24f8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24f8f-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="24f8f-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="24f8f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24f8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24f8f-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24f8f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24f8f-128">Header</span><span class="sxs-lookup"><span data-stu-id="24f8f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f8f-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="24f8f-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24f8f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24f8f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f8f-131">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24f8f-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
