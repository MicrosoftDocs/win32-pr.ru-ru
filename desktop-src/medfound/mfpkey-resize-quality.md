---
description: Указывает, следует ли использовать алгоритм, создающий видео более высокого качества, или более быстрый алгоритм.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Свойство MFPKEY_RESIZE_QUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711778"
---
# <a name="mfpkey_resize_quality-property"></a><span data-ttu-id="277b1-103">МФПКЭЙ \_ изменить \_ свойство качества</span><span class="sxs-lookup"><span data-stu-id="277b1-103">MFPKEY\_RESIZE\_QUALITY Property</span></span>

<span data-ttu-id="277b1-104">Указывает, следует ли использовать алгоритм, создающий видео более высокого качества, или более быстрый алгоритм.</span><span class="sxs-lookup"><span data-stu-id="277b1-104">Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="277b1-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="277b1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="277b1-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="277b1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="277b1-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="277b1-107">Data Type</span></span>

<span data-ttu-id="277b1-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="277b1-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="277b1-109">Применение</span><span class="sxs-lookup"><span data-stu-id="277b1-109">Applies To</span></span>

-   [<span data-ttu-id="277b1-110">DSP изменения видеоконтроллеров</span><span class="sxs-lookup"><span data-stu-id="277b1-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="277b1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="277b1-111">Remarks</span></span>

<span data-ttu-id="277b1-112">Используйте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="277b1-112">Use one of the following values:</span></span>



| <span data-ttu-id="277b1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="277b1-113">Value</span></span>     | <span data-ttu-id="277b1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="277b1-114">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="277b1-115">VT \_ false</span><span class="sxs-lookup"><span data-stu-id="277b1-115">VT\_FALSE</span></span> | <span data-ttu-id="277b1-116">Более быстрый алгоритм</span><span class="sxs-lookup"><span data-stu-id="277b1-116">Faster algorithm</span></span>     |
| <span data-ttu-id="277b1-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="277b1-117">VT\_TRUE</span></span>  | <span data-ttu-id="277b1-118">Видео высокого качества</span><span class="sxs-lookup"><span data-stu-id="277b1-118">Higher-quality video</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="277b1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="277b1-119">Requirements</span></span>



| <span data-ttu-id="277b1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="277b1-120">Requirement</span></span> | <span data-ttu-id="277b1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="277b1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="277b1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="277b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="277b1-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="277b1-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="277b1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="277b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="277b1-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="277b1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="277b1-126">Header</span><span class="sxs-lookup"><span data-stu-id="277b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="277b1-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="277b1-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277b1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="277b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277b1-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="277b1-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
