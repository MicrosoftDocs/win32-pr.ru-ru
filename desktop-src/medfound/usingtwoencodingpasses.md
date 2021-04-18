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
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Использование кодировки Two-Pass (Microsoft Media Foundation)

Двухстороннее кодирование можно использовать для постоянной скорости потока (CBR) и для кодирования с переменной скоростью (VBR) с помощью некоторых кодеков Windows Media. Максимальное число проходов кодирования, поддерживаемое кодеком, можно получить, извлекая свойство [мфпкэй \_ пассесрекоммендед](mfpkey-passesrecommendedproperty.md) . Ни один из кодеков не поддерживает более двух проходов. Настройте DMO для использования двух проходов, задав для свойства [мфпкэй \_ пассесусед](mfpkey-passesusedproperty.md) значение 2.

Доставьте образцы в кодировщик DMO по одному за раз, как в однопроходном режиме. При обработке входных примеров для этапа предварительной обработки вызовы [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) или [**Имфтрансформ::P Роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) возвратит **\_ значение S false**, чтобы указать, что выходные данные не создаются.

В конце первого прохода (после первой обработки последнего ввода) необходимо задать свойство [мфпкэй \_ ендофпасс](mfpkey-endofpassproperty.md) , чтобы уведомить кодек о том, что следующий обработанный ввод является первым входом второго прохода. Для этого свойства значение не требуется, поэтому следует использовать пустую структуру **Variant** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Кодеки Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
