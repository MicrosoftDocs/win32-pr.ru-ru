---
description: Указывает фрагменты содержимого, которые должны быть закодированы голосовым кодеком в качестве музыки.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Свойство MFPKEY_WMAVOICE_ENC_EDL (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812629"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="63a06-103">МФПКЭЙ \_ вмавоице \_ ENC, \_ свойство ЕДЛ</span><span class="sxs-lookup"><span data-stu-id="63a06-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="63a06-104">Указывает фрагменты содержимого, которые должны быть закодированы голосовым кодеком в качестве музыки.</span><span class="sxs-lookup"><span data-stu-id="63a06-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="63a06-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="63a06-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="63a06-106">g \_ всзвмаквоицебуффер</span><span class="sxs-lookup"><span data-stu-id="63a06-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="63a06-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="63a06-107">Data Type</span></span>

<span data-ttu-id="63a06-108">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="63a06-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="63a06-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="63a06-109">Default Value</span></span>

<span data-ttu-id="63a06-110">Нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63a06-110">No default value.</span></span> <span data-ttu-id="63a06-111">Если это свойство не задано, кодек будет использовать значение свойства [мфпкэй \_ вмавоице \_ ENC \_ мусикспичклассмоде](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) , чтобы определить способ кодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="63a06-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a06-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63a06-112">Remarks</span></span>

<span data-ttu-id="63a06-113">Это свойство можно использовать, если автоматический режим кодека не дает удовлетворительных результатов.</span><span class="sxs-lookup"><span data-stu-id="63a06-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="63a06-114">Это значение представляет собой строку с разделителями-запятыми, содержащую не менее четырех целых чисел.</span><span class="sxs-lookup"><span data-stu-id="63a06-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="63a06-115">Первое целое число — это номер версии; всегда используйте 1 для этого значения.</span><span class="sxs-lookup"><span data-stu-id="63a06-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="63a06-116">Второе целое число — это количество разделов, которые необходимо закодировать как музыку.</span><span class="sxs-lookup"><span data-stu-id="63a06-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="63a06-117">За вторым целым числом является число пар значений, представляющих диапазоны в миллисекундах, одну пару для каждого раздела содержимого, которую необходимо закодировать как музыку.</span><span class="sxs-lookup"><span data-stu-id="63a06-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="63a06-118">Например, "1, 2100200500600" информирует кодировщик о необходимости использовать версию 1 с 2 разделами музыки.</span><span class="sxs-lookup"><span data-stu-id="63a06-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="63a06-119">Первый раздел музыки начинается с 100 мс и заканчивается на 200 мс.</span><span class="sxs-lookup"><span data-stu-id="63a06-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="63a06-120">Второй раздел музыки начинается с 500 мс и заканчивается на 600 мс.</span><span class="sxs-lookup"><span data-stu-id="63a06-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a06-121">Требования</span><span class="sxs-lookup"><span data-stu-id="63a06-121">Requirements</span></span>



| <span data-ttu-id="63a06-122">Требование</span><span class="sxs-lookup"><span data-stu-id="63a06-122">Requirement</span></span> | <span data-ttu-id="63a06-123">Значение</span><span class="sxs-lookup"><span data-stu-id="63a06-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63a06-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63a06-124">Minimum supported client</span></span><br/> | <span data-ttu-id="63a06-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="63a06-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="63a06-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63a06-126">Minimum supported server</span></span><br/> | <span data-ttu-id="63a06-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63a06-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63a06-128">Header</span><span class="sxs-lookup"><span data-stu-id="63a06-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="63a06-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a06-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a06-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63a06-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a06-131">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63a06-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




