---
description: Указывает требуемый максимальный уровень громкости выходного аудио содержимого.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Свойство MFPKEY_WMADRC_PEAKTARGET (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692800"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="c9f19-103">МФПКЭЙ \_ вмадрк \_ Пеактаржет, свойство</span><span class="sxs-lookup"><span data-stu-id="c9f19-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="c9f19-104">Указывает требуемый максимальный уровень громкости выходного аудио содержимого.</span><span class="sxs-lookup"><span data-stu-id="c9f19-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c9f19-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="c9f19-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c9f19-106">g \_ всзвмадркпеактаржет</span><span class="sxs-lookup"><span data-stu-id="c9f19-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="c9f19-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c9f19-107">Data Type</span></span>

<span data-ttu-id="c9f19-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c9f19-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c9f19-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c9f19-109">Default Value</span></span>

<span data-ttu-id="c9f19-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c9f19-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f19-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9f19-111">Remarks</span></span>

<span data-ttu-id="c9f19-112">Это значение можно задать для декодера в целях динамического управления диапазоном, но оно будет действовать, только если задано свойство [мфпкэй \_ вмадек \_ дркмоде](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f19-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="c9f19-113">При запросе динамического элемента управления диапазоном от декодера, если это свойство не задано, кодек вычислит значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9f19-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="c9f19-114">Используйте свойства [мфпкэй \_ вмадрк \_ авгреф](mfpkey-wmadrc-avgrefproperty.md) и [мфпкэй \_ вмадрк \_ пеакреф](mfpkey-wmadrc-peakrefproperty.md) , чтобы вычислить соответствующие значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c9f19-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="c9f19-115">Дополнительные сведения об управлении динамическими диапазонами см. в статье о [функциях кодеков Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10))в Интернете.</span><span class="sxs-lookup"><span data-stu-id="c9f19-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f19-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c9f19-116">Requirements</span></span>



| <span data-ttu-id="c9f19-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c9f19-117">Requirement</span></span> | <span data-ttu-id="c9f19-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c9f19-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f19-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9f19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f19-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9f19-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c9f19-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9f19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f19-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9f19-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9f19-123">Header</span><span class="sxs-lookup"><span data-stu-id="c9f19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9f19-124"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f19-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9f19-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9f19-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f19-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9f19-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
