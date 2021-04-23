---
description: Указывает, ограничивается ли кодировщик максимальным требованием к задержке.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: Свойство MFPKEY_CONSTRAINENCLATENCY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692858"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="ee032-103">МФПКЭЙ \_ констраиненклатенци, свойство</span><span class="sxs-lookup"><span data-stu-id="ee032-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="ee032-104">Указывает, ограничивается ли кодировщик максимальным требованием к задержке.</span><span class="sxs-lookup"><span data-stu-id="ee032-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ee032-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="ee032-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ee032-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="ee032-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ee032-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ee032-107">Data Type</span></span>

<span data-ttu-id="ee032-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="ee032-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="ee032-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ee032-109">Default Value</span></span>

<span data-ttu-id="ee032-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="ee032-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="ee032-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee032-111">Remarks</span></span>

<span data-ttu-id="ee032-112">Если оставить это свойство по умолчанию со значением **Variant \_ false**, кодировщик перечислит набор режимов по умолчанию примерно 2000 миллисекунд для задержки кодировщика.</span><span class="sxs-lookup"><span data-stu-id="ee032-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="ee032-113">Если для этого свойства задать значение **\_ true**, необходимо также указать максимальную задержку кодировщика, задав свойство [**мфпкэй \_ максенклатенцимс**](mfpkey-maxenclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ee032-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="ee032-114">В этом случае кодировщик создает режимы, которые отвечают требованиям к задержке, и перечисляет только эти режимы.</span><span class="sxs-lookup"><span data-stu-id="ee032-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="ee032-115">Кодировщик гарантирует выборку выходных данных, как только кодировщик получил входные данные за период времени, равный **мфпкэй \_ максенклатенцимс**.</span><span class="sxs-lookup"><span data-stu-id="ee032-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee032-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ee032-116">Requirements</span></span>



| <span data-ttu-id="ee032-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ee032-117">Requirement</span></span> | <span data-ttu-id="ee032-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ee032-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee032-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee032-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee032-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee032-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ee032-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee032-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee032-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee032-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee032-123">Header</span><span class="sxs-lookup"><span data-stu-id="ee032-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee032-124"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee032-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee032-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee032-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee032-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee032-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
