---
description: Указывает требуемый средний уровень громкости выходного звукового содержимого.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Свойство MFPKEY_WMADRC_AVGTARGET (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263901"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="c956a-103">МФПКЭЙ \_ вмадрк \_ Авгтаржет, свойство</span><span class="sxs-lookup"><span data-stu-id="c956a-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="c956a-104">Указывает требуемый средний уровень громкости выходного звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="c956a-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c956a-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="c956a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c956a-106">g \_ всзвмадркаверажетаржет</span><span class="sxs-lookup"><span data-stu-id="c956a-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="c956a-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c956a-107">Data Type</span></span>

<span data-ttu-id="c956a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c956a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c956a-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c956a-109">Default Value</span></span>

<span data-ttu-id="c956a-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c956a-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="c956a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c956a-111">Remarks</span></span>

<span data-ttu-id="c956a-112">Это значение можно задать для декодера в целях динамического управления диапазоном, но оно будет действовать, только если задано свойство [мфпкэй \_ вмадек \_ дркмоде](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="c956a-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="c956a-113">Установка среднего значения целевого объекта не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c956a-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="c956a-114">Настройка среднего значения не влияет на разницу между громкими и мягкими звуками.</span><span class="sxs-lookup"><span data-stu-id="c956a-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="c956a-115">Вместо этого он вырезает или увеличивает общий средний объем, что может привести к нежелательному искажению во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c956a-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="c956a-116">При запросе динамического элемента управления диапазоном от декодера, если это свойство не задано, кодек вычислит значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c956a-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="c956a-117">Используйте свойства [мфпкэй \_ вмадрк \_ авгреф](mfpkey-wmadrc-avgrefproperty.md) и [мфпкэй \_ вмадрк \_ пеакреф](mfpkey-wmadrc-peakrefproperty.md) , чтобы вычислить соответствующие значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c956a-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c956a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c956a-118">Requirements</span></span>



| <span data-ttu-id="c956a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c956a-119">Requirement</span></span> | <span data-ttu-id="c956a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c956a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c956a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c956a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c956a-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c956a-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c956a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c956a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c956a-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c956a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c956a-125">Header</span><span class="sxs-lookup"><span data-stu-id="c956a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c956a-126"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c956a-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c956a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c956a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c956a-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c956a-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




