---
description: Указывает, ограничивается ли кодировщик максимальным требованием к задержке декодера.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Свойство MFPKEY_CONSTRAINDECLATENCY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692859"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="e3731-103">МФПКЭЙ \_ констраиндеклатенци, свойство</span><span class="sxs-lookup"><span data-stu-id="e3731-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="e3731-104">Указывает, ограничивается ли кодировщик максимальным требованием к задержке декодера.</span><span class="sxs-lookup"><span data-stu-id="e3731-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e3731-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="e3731-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e3731-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e3731-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e3731-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e3731-107">Data Type</span></span>

<span data-ttu-id="e3731-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="e3731-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="e3731-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e3731-109">Default Value</span></span>

<span data-ttu-id="e3731-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="e3731-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3731-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3731-111">Remarks</span></span>

<span data-ttu-id="e3731-112">Если оставить это свойство по умолчанию со значением **Variant \_ false**, кодировщик перечислит набор режимов по умолчанию примерно 1500 миллисекунд для задержки декодера.</span><span class="sxs-lookup"><span data-stu-id="e3731-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="e3731-113">Если для этого свойства задать значение **\_ true**, необходимо также указать максимальную задержку декодера, задав свойство [**мфпкэй \_ максдеклатенцимс**](mfpkey-maxdeclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e3731-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="e3731-114">В этом случае кодировщик создает режимы, которые отвечают требованиям к задержке, и перечисляет только эти режимы.</span><span class="sxs-lookup"><span data-stu-id="e3731-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="e3731-115">Кодировщик гарантирует, что преддостаточные требования (размер буфера декодера) меньше или равны **мфпкэй \_ максдеклатенцимс**.</span><span class="sxs-lookup"><span data-stu-id="e3731-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3731-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e3731-116">Requirements</span></span>



| <span data-ttu-id="e3731-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e3731-117">Requirement</span></span> | <span data-ttu-id="e3731-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e3731-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3731-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3731-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3731-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3731-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3731-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3731-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3731-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3731-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3731-123">Header</span><span class="sxs-lookup"><span data-stu-id="e3731-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3731-124"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3731-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3731-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3731-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3731-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3731-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
