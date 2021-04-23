---
description: Двухстороннее кодирование можно использовать для постоянной скорости потока (CBR) и для кодирования с переменной скоростью (VBR) с помощью некоторых кодеков Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Использование кодировки Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683210"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="0c670-103">Использование кодировки Two-Pass (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="0c670-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="0c670-104">Двухстороннее кодирование можно использовать для постоянной скорости потока (CBR) и для кодирования с переменной скоростью (VBR) с помощью некоторых кодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0c670-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="0c670-105">Максимальное число проходов кодирования, поддерживаемое кодеком, можно получить, извлекая свойство [мфпкэй \_ пассесрекоммендед](mfpkey-passesrecommendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0c670-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="0c670-106">Ни один из кодеков не поддерживает более двух проходов.</span><span class="sxs-lookup"><span data-stu-id="0c670-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="0c670-107">Настройте DMO для использования двух проходов, задав для свойства [мфпкэй \_ пассесусед](mfpkey-passesusedproperty.md) значение 2.</span><span class="sxs-lookup"><span data-stu-id="0c670-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="0c670-108">Доставьте образцы в кодировщик DMO по одному за раз, как в однопроходном режиме.</span><span class="sxs-lookup"><span data-stu-id="0c670-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="0c670-109">При обработке входных примеров для этапа предварительной обработки вызовы [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) или [**Имфтрансформ::P Роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) возвратит **\_ значение S false**, чтобы указать, что выходные данные не создаются.</span><span class="sxs-lookup"><span data-stu-id="0c670-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="0c670-110">В конце первого прохода (после первой обработки последнего ввода) необходимо задать свойство [мфпкэй \_ ендофпасс](mfpkey-endofpassproperty.md) , чтобы уведомить кодек о том, что следующий обработанный ввод является первым входом второго прохода.</span><span class="sxs-lookup"><span data-stu-id="0c670-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="0c670-111">Для этого свойства значение не требуется, поэтому следует использовать пустую структуру **Variant** .</span><span class="sxs-lookup"><span data-stu-id="0c670-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c670-112">См. также</span><span class="sxs-lookup"><span data-stu-id="0c670-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c670-113">Кодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="0c670-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
