---
description: Указывает сложность алгоритма кодирования.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Свойство MFPKEY_ENCCOMPLEXITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908783"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="35563-103">МФПКЭЙ \_ енккомплексити, свойство</span><span class="sxs-lookup"><span data-stu-id="35563-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="35563-104">Указывает сложность алгоритма кодирования.</span><span class="sxs-lookup"><span data-stu-id="35563-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="35563-105">Значение является целым числом от 0 до 100, где 0 указывает наименьший сложный алгоритм, а 100 — наиболее сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="35563-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="35563-106">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="35563-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="35563-107">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="35563-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="35563-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="35563-108">Data Type</span></span>

<span data-ttu-id="35563-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="35563-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="35563-110">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="35563-110">Default Value</span></span>

<span data-ttu-id="35563-111">100 для Windows Media Audio 10 и Windows Media Audio 10 профессиональная</span><span class="sxs-lookup"><span data-stu-id="35563-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="35563-112">100. выпуск Windows Media Audio 10 без потерь для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35563-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="35563-113">0 для выпуска Windows Media Audio 10 без потерь</span><span class="sxs-lookup"><span data-stu-id="35563-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="35563-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35563-114">Remarks</span></span>

<span data-ttu-id="35563-115">Если свойство [**мфпкэй \_ констраинекомплексити**](mfpkey-constrainenccomplexityproperty.md) имеет значение **Variant \_ true**, кодировщик корректирует сложность его алгоритма в соответствии со значением этого свойства.</span><span class="sxs-lookup"><span data-stu-id="35563-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="35563-116">Для кодировщика Windows Media Audio 10 и кодировщика Windows Media Audio 10 Professional, если значение этого свойства равно 100, кодировщик помещает высокую нагрузку на ЦП и выдает наивысшее качество вывода.</span><span class="sxs-lookup"><span data-stu-id="35563-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="35563-117">По мере уменьшения значения этого свойства потребность в ЦП снижается, но качество вывода также уменьшается.</span><span class="sxs-lookup"><span data-stu-id="35563-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="35563-118">Для кодировщика Windows Media Audio 10 без потерь, если значение этого свойства равно 0, кодировщик помещает низкий спрос на ЦП.</span><span class="sxs-lookup"><span data-stu-id="35563-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="35563-119">По мере увеличения значения этого свойства потребность в ЦП увеличивается, а размер выходных данных кодировщика немного сокращается.</span><span class="sxs-lookup"><span data-stu-id="35563-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="35563-120">Выходные данные без потерь зависят от значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="35563-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="35563-121">Если оставить это свойство по умолчанию со значением **Variant \_ false**, кодировщик использует алгоритм по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35563-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="35563-122">Алгоритм по умолчанию зависит от используемого кодировщика и версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="35563-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="35563-123">В следующей таблице описывается поведение по умолчанию для различных сочетаний.</span><span class="sxs-lookup"><span data-stu-id="35563-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="35563-124">Операционная система</span><span class="sxs-lookup"><span data-stu-id="35563-124">Operating system</span></span> | <span data-ttu-id="35563-125">Поведение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="35563-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35563-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35563-126">Windows Vista</span></span>    | <span data-ttu-id="35563-127">Кодировщики Windows Media Audio 10, Windows Media Audio 10 Professional и Windows Media Audio 10 без потерь по умолчанию используют самый сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="35563-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="35563-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35563-128">Windows 7</span></span>        | <span data-ttu-id="35563-129">Кодировщики Windows Media Audio 10 и Windows Media Audio 10 Professional по умолчанию используют самый сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="35563-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="35563-130">Кодировщик Windows Media Audio 10 без потерь по умолчанию использует самый сложный алгоритм.</span><span class="sxs-lookup"><span data-stu-id="35563-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="35563-131">Если свойство [**\_ констраинекомплексити мфпкэй**](mfpkey-constrainenccomplexityproperty.md) имеет значение **Variant \_ false**, кодировщик игнорирует это свойство.</span><span class="sxs-lookup"><span data-stu-id="35563-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="35563-132">Требования</span><span class="sxs-lookup"><span data-stu-id="35563-132">Requirements</span></span>



| <span data-ttu-id="35563-133">Требование</span><span class="sxs-lookup"><span data-stu-id="35563-133">Requirement</span></span> | <span data-ttu-id="35563-134">Значение</span><span class="sxs-lookup"><span data-stu-id="35563-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35563-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35563-135">Minimum supported client</span></span><br/> | <span data-ttu-id="35563-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35563-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35563-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35563-137">Minimum supported server</span></span><br/> | <span data-ttu-id="35563-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35563-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35563-139">Header</span><span class="sxs-lookup"><span data-stu-id="35563-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="35563-140"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="35563-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35563-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35563-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35563-142">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35563-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
