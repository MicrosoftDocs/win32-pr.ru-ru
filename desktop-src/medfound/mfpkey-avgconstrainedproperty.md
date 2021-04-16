---
description: Указывает, использует ли кодировщик среднее-управляемое кодирование VBR.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Свойство MFPKEY_AVGCONSTRAINED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692246"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="79d3f-103">МФПКЭЙ \_ авгконстраинед, свойство</span><span class="sxs-lookup"><span data-stu-id="79d3f-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="79d3f-104">Указывает, использует ли кодировщик среднее-управляемое кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="79d3f-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="79d3f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="79d3f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="79d3f-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="79d3f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="79d3f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="79d3f-107">Data Type</span></span>

<span data-ttu-id="79d3f-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="79d3f-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="79d3f-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79d3f-109">Default Value</span></span>

<span data-ttu-id="79d3f-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="79d3f-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="79d3f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79d3f-111">Remarks</span></span>

<span data-ttu-id="79d3f-112">Если для этого свойства и [**свойства \_ вбренаблед мфпкэй**](mfpkey-vbrenabledproperty.md) задано значение **Variant \_ true**, кодировщик использует среднее-управляемое кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="79d3f-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="79d3f-113">В этом случае кодировщик настраивает себя в соответствии со значениями [**мфпкэй \_ Дин \_ VBR \_ бавг**](mfpkey-dyn-vbr-bavgproperty.md) и [**мфпкэй \_ Дин \_ VBR \_ равг**](mfpkey-dyn-vbr-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="79d3f-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79d3f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="79d3f-114">Requirements</span></span>



| <span data-ttu-id="79d3f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="79d3f-115">Requirement</span></span> | <span data-ttu-id="79d3f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="79d3f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79d3f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79d3f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79d3f-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79d3f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="79d3f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79d3f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79d3f-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79d3f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79d3f-121">Header</span><span class="sxs-lookup"><span data-stu-id="79d3f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="79d3f-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d3f-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d3f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79d3f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d3f-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79d3f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
