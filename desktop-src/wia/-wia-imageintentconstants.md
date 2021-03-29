---
description: Константы намерения образа определяют тип данных, которые должно представлять изображение.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Константы с намерением изображения (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991278"
---
# <a name="image-intent-constants"></a><span data-ttu-id="a7f7c-103">Константы намерения образа</span><span class="sxs-lookup"><span data-stu-id="a7f7c-103">Image Intent Constants</span></span>

<span data-ttu-id="a7f7c-104">Константы намерения образа определяют тип данных, которые должно представлять изображение.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="a7f7c-105">Свойство [**сканирования \_ IP-адресов с \_ \_ намерением "WIA**](-wia-wiaitempropscanneritem.md) " использует эти флаги.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="a7f7c-106">Чтобы обеспечить намерение, объедините предустановленный флаг типа изображения с нужным флагом размера или качества с помощью оператора или.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="a7f7c-107">\_Цель WIA \_ None не должна сочетаться с другими флагами.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="a7f7c-108">Обратите внимание, что изображение не может одновременно иметь оттенки серого и цвета.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="a7f7c-109">Ниже приведены допустимые константы намерения образа.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="a7f7c-110">Предназначенные флаги типа образа</span><span class="sxs-lookup"><span data-stu-id="a7f7c-110">Intended image type flags</span></span>           | <span data-ttu-id="a7f7c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a7f7c-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="a7f7c-112">\_Цель WIA \_ None</span><span class="sxs-lookup"><span data-stu-id="a7f7c-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="a7f7c-113">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-113">Default value.</span></span> <span data-ttu-id="a7f7c-114">Не предустановки никаких свойств.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="a7f7c-115">\_ \_ \_ Цвет типа изображения с намерением WIA \_</span><span class="sxs-lookup"><span data-stu-id="a7f7c-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="a7f7c-116">Предустановленные свойства для цветового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="a7f7c-117">\_ \_ тип изображения с НАМЕРЕНием WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7f7c-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="a7f7c-118">Предустановленные свойства для содержимого в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="a7f7c-119">\_ \_ \_ текст типа изображения с намерением WIA \_</span><span class="sxs-lookup"><span data-stu-id="a7f7c-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="a7f7c-120">Предустановленные свойства для текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="a7f7c-121">\_ \_ \_ маска типа изображения с намерением WIA \_</span><span class="sxs-lookup"><span data-stu-id="a7f7c-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="a7f7c-122">Маска для всех флагов типа изображения.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="a7f7c-123">Предполагаемый размер изображения/флаги качества</span><span class="sxs-lookup"><span data-stu-id="a7f7c-123">Intended image size/quality flags</span></span> | <span data-ttu-id="a7f7c-124">Описание</span><span class="sxs-lookup"><span data-stu-id="a7f7c-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="a7f7c-125">Цель WIA — \_ \_ Минимальный \_ Размер</span><span class="sxs-lookup"><span data-stu-id="a7f7c-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="a7f7c-126">Предустановленные свойства для сворачивания размера изображения.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="a7f7c-127">\_развертывание с намерением WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7f7c-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="a7f7c-128">Предустановленные свойства для повышения качества изображения.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="a7f7c-129">\_Маска размера намерений WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7f7c-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="a7f7c-130">Маска для всех флагов размера и качества.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="a7f7c-131">\_ \_ лучшее \_ предварительное ознакомление с намерением WIA</span><span class="sxs-lookup"><span data-stu-id="a7f7c-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="a7f7c-132">Задает наилучшее качество предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="a7f7c-133">В следующем списке показано имя константы C/C++, за которым следует соответствующее имя в круглых скобках, используемое в скриптах.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="a7f7c-134">Имена сценариев относятся к перечисляемому типу Виаинтент.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="a7f7c-135">Обратите внимание, что не все константы доступны в скрипте.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="a7f7c-136">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="a7f7c-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="a7f7c-137">Описание</span><span class="sxs-lookup"><span data-stu-id="a7f7c-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="a7f7c-138"><dt>**WIA \_ \_Тип образа намерения, \_ \_ Цвет**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="a7f7c-139">Предустановленные свойства для цветового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="a7f7c-140"><dt>**WIA \_ \_Тип образа намерения — \_ \_ градации серого**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="a7f7c-141">Предустановленные свойства для содержимого в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="a7f7c-142"><dt>**WIA \_ \_Тип образа намерения, \_ \_ текст**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="a7f7c-143">Предустановленные свойства для текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="a7f7c-144"><dt>**WIA \_ НАМЕРЕНие \_ сокращать \_ Размер**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="a7f7c-145">Предустановленные свойства для сворачивания размера изображения.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="a7f7c-146"><dt>**WIA \_ Преднамерение \_ максимизировать \_ качество**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="a7f7c-147">Предустановленные свойства для повышения качества изображения.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="a7f7c-148"><dt>**WIA \_ Преднамеренный \_ \_ Предварительный просмотр**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="a7f7c-149">Задает наилучшее качество предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="a7f7c-150">Требования</span><span class="sxs-lookup"><span data-stu-id="a7f7c-150">Requirements</span></span>



| <span data-ttu-id="a7f7c-151">Требование</span><span class="sxs-lookup"><span data-stu-id="a7f7c-151">Requirement</span></span> | <span data-ttu-id="a7f7c-152">Значение</span><span class="sxs-lookup"><span data-stu-id="a7f7c-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f7c-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7f7c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f7c-154">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a7f7c-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a7f7c-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7f7c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f7c-156">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7f7c-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a7f7c-157">Header</span><span class="sxs-lookup"><span data-stu-id="a7f7c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f7c-158"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f7c-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




