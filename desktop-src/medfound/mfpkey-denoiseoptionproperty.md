---
description: Указывает, будет ли кодек использовать фильтр шума при кодировании.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Свойство MFPKEY_DENOISEOPTION (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647288"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="52e09-103">МФПКЭЙ \_ деноисеоптион, свойство</span><span class="sxs-lookup"><span data-stu-id="52e09-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="52e09-104">Указывает, будет ли кодек использовать фильтр шума при кодировании.</span><span class="sxs-lookup"><span data-stu-id="52e09-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="52e09-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="52e09-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="52e09-106">g \_ всзвмвкденоисеоптион</span><span class="sxs-lookup"><span data-stu-id="52e09-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="52e09-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="52e09-107">Data Type</span></span>

<span data-ttu-id="52e09-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="52e09-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="52e09-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="52e09-109">Default Value</span></span>

<span data-ttu-id="52e09-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="52e09-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="52e09-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52e09-111">Remarks</span></span>

<span data-ttu-id="52e09-112">Фильтр шума может улучшить качество звуковых источников, таких как фильм, содержащий много граней или снимка видео, на низком свете.</span><span class="sxs-lookup"><span data-stu-id="52e09-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="52e09-113">Этот фильтр можно использовать в сценариях кодирования в реальном времени, когда внешняя Предварительная обработка не является вариантом.</span><span class="sxs-lookup"><span data-stu-id="52e09-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="52e09-114">Этот фильтр должен быть отключен для чистых видеороликов, так как он может уменьшить качество изображения, когда качество подходит для начала.</span><span class="sxs-lookup"><span data-stu-id="52e09-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e09-115">Требования</span><span class="sxs-lookup"><span data-stu-id="52e09-115">Requirements</span></span>



| <span data-ttu-id="52e09-116">Требование</span><span class="sxs-lookup"><span data-stu-id="52e09-116">Requirement</span></span> | <span data-ttu-id="52e09-117">Значение</span><span class="sxs-lookup"><span data-stu-id="52e09-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52e09-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52e09-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52e09-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="52e09-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="52e09-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52e09-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52e09-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52e09-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52e09-122">Header</span><span class="sxs-lookup"><span data-stu-id="52e09-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52e09-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="52e09-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e09-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52e09-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e09-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52e09-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




