---
description: Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Свойство MFPKEY_DYN_VBR_RAVG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991607"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="e86ef-103">МФПКЭЙ \_ Дин \_ VBR \_ равг, свойство</span><span class="sxs-lookup"><span data-stu-id="e86ef-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="e86ef-104">Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="e86ef-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e86ef-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="e86ef-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e86ef-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e86ef-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e86ef-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e86ef-107">Data Type</span></span>

<span data-ttu-id="e86ef-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="e86ef-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="e86ef-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e86ef-109">Remarks</span></span>

<span data-ttu-id="e86ef-110">Если для свойств [**мфпкэй \_ Авгконстраинед**](mfpkey-avgconstrainedproperty.md) и [**мфпкэй \_ вбренаблед**](mfpkey-vbrenabledproperty.md) задано значение **Variant \_ true**, кодировщик использует среднюю управляемую кодировку VBR.</span><span class="sxs-lookup"><span data-stu-id="e86ef-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="e86ef-111">В этом случае кодировщик настраивает себя в соответствии со значением этого свойства и свойством [**мфпкэй \_ Дин \_ VBR \_ бавг**](mfpkey-dyn-vbr-bavgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e86ef-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86ef-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e86ef-112">Requirements</span></span>



| <span data-ttu-id="e86ef-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e86ef-113">Requirement</span></span> | <span data-ttu-id="e86ef-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e86ef-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e86ef-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e86ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e86ef-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e86ef-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e86ef-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e86ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e86ef-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e86ef-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e86ef-119">Header</span><span class="sxs-lookup"><span data-stu-id="e86ef-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e86ef-120"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e86ef-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86ef-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e86ef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86ef-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e86ef-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
