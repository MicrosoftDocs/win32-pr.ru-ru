---
description: Указывает, использует ли кодировщик кодирование с переменной скоростью (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Свойство MFPKEY_VBRENABLED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908747"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="1b0c4-103">МФПКЭЙ \_ вбренаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="1b0c4-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="1b0c4-104">Указывает, использует ли кодировщик кодирование с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="1b0c4-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="1b0c4-105">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="1b0c4-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1b0c4-106">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1b0c4-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="1b0c4-107">**g \_ всзвмвквбренаблед**, **g \_ всзвмкпаудиовбрсуппортед**</span><span class="sxs-lookup"><span data-stu-id="1b0c4-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="1b0c4-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1b0c4-108">Data Type</span></span>

<span data-ttu-id="1b0c4-109">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="1b0c4-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="1b0c4-110">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1b0c4-110">Default Value</span></span>

<span data-ttu-id="1b0c4-111">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="1b0c4-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b0c4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b0c4-112">Remarks</span></span>

<span data-ttu-id="1b0c4-113">Это значение должно быть равно **\_ true** для любого из других свойств VBR, используемых кодеком.</span><span class="sxs-lookup"><span data-stu-id="1b0c4-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="1b0c4-114">После присвоения этому значению **значения \_ true** в звуковом кодировщике типы выходных данных, полученные с помощью метода [**имедиаобжект:: ЖЕТАУТПУТТИПЕ**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) , имеют тип VBR.</span><span class="sxs-lookup"><span data-stu-id="1b0c4-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b0c4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1b0c4-115">Requirements</span></span>



| <span data-ttu-id="1b0c4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1b0c4-116">Requirement</span></span> | <span data-ttu-id="1b0c4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1b0c4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b0c4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b0c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b0c4-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1b0c4-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1b0c4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b0c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b0c4-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b0c4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b0c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="1b0c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b0c4-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b0c4-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b0c4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b0c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b0c4-125">**МФПКЭЙ \_ ограничение \_ перечисления \_ вбркуалити**</span><span class="sxs-lookup"><span data-stu-id="1b0c4-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="1b0c4-126">**МФПКЭЙ \_ желаемый \_ вбркуалити**</span><span class="sxs-lookup"><span data-stu-id="1b0c4-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="1b0c4-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b0c4-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
