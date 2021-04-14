---
description: Указывает окно буфера (в миллисекундах) для кодировщика, который настроен для использования среднего управляемого кодирования VBR.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: Свойство MFPKEY_DYN_VBR_BAVG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647285"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a><span data-ttu-id="d01da-103">МФПКЭЙ \_ Дин \_ VBR \_ бавг, свойство</span><span class="sxs-lookup"><span data-stu-id="d01da-103">MFPKEY\_DYN\_VBR\_BAVG Property</span></span>

<span data-ttu-id="d01da-104">Указывает окно буфера (в миллисекундах) для кодировщика, который настроен для использования среднего управляемого кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="d01da-104">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d01da-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="d01da-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d01da-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d01da-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d01da-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d01da-107">Data Type</span></span>

<span data-ttu-id="d01da-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d01da-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="d01da-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d01da-109">Remarks</span></span>

<span data-ttu-id="d01da-110">Если для свойств [**мфпкэй \_ Авгконстраинед**](mfpkey-avgconstrainedproperty.md) и [**мфпкэй \_ вбренаблед**](mfpkey-vbrenabledproperty.md) задано значение **Variant \_ true**, кодировщик использует среднюю управляемую кодировку VBR.</span><span class="sxs-lookup"><span data-stu-id="d01da-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="d01da-111">В этом случае кодировщик настраивает себя в соответствии со значением этого свойства и свойством [**мфпкэй \_ Дин \_ VBR \_ равг**](mfpkey-dyn-vbr-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d01da-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01da-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d01da-112">Requirements</span></span>



| <span data-ttu-id="d01da-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d01da-113">Requirement</span></span> | <span data-ttu-id="d01da-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d01da-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d01da-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d01da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d01da-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d01da-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d01da-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d01da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d01da-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d01da-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d01da-119">Header</span><span class="sxs-lookup"><span data-stu-id="d01da-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d01da-120"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d01da-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01da-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d01da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01da-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d01da-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
