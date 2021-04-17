---
description: Задает режим работы с голосовым кодеком.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Свойство MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692592"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="419d2-103">МФПКЭЙ \_ вмавоице \_ ENC, \_ свойство мусикспичклассмоде</span><span class="sxs-lookup"><span data-stu-id="419d2-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="419d2-104">Задает режим работы с голосовым кодеком.</span><span class="sxs-lookup"><span data-stu-id="419d2-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="419d2-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="419d2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="419d2-106">g \_ всзвмакмусикспичклассмоде</span><span class="sxs-lookup"><span data-stu-id="419d2-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="419d2-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="419d2-107">Data Type</span></span>

<span data-ttu-id="419d2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="419d2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="419d2-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="419d2-109">Default Value</span></span>

<span data-ttu-id="419d2-110">1</span><span class="sxs-lookup"><span data-stu-id="419d2-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="419d2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="419d2-111">Remarks</span></span>

<span data-ttu-id="419d2-112">Значение 1 информирует кодек о том, что содержимое является только голосовым, значение 2 имеет кодек для автоматического определения режима, а любое другое значение информирует кодек о необходимости использования музыкального режима.</span><span class="sxs-lookup"><span data-stu-id="419d2-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="419d2-113">Если в автоматическом режиме не выполняется правильная кодировка смешанного голоса и музыки, можно указать кодировку для отдельных разделов файла с помощью свойства [мфпкэй \_ вмавоице \_ ENC \_ ЕДЛ](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="419d2-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="419d2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="419d2-114">Requirements</span></span>



| <span data-ttu-id="419d2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="419d2-115">Requirement</span></span> | <span data-ttu-id="419d2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="419d2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="419d2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="419d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="419d2-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="419d2-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="419d2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="419d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="419d2-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="419d2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="419d2-121">Header</span><span class="sxs-lookup"><span data-stu-id="419d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="419d2-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="419d2-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="419d2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="419d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419d2-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="419d2-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




