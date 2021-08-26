---
description: двухстороннее кодирование можно использовать для постоянной скорости потока (CBR) и для кодирования с переменной скоростью (VBR) с помощью некоторых кодеков Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Использование кодировки Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a79678e3b4396dfe87b93dfda7c9fd26487b8fdba83d2214509675ee742951
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887114"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Использование кодировки Two-Pass (Microsoft Media Foundation)

двухстороннее кодирование можно использовать для постоянной скорости потока (CBR) и для кодирования с переменной скоростью (VBR) с помощью некоторых кодеков Windows Media. Максимальное число проходов кодирования, поддерживаемое кодеком, можно получить, извлекая свойство [мфпкэй \_ пассесрекоммендед](mfpkey-passesrecommendedproperty.md) . Ни один из кодеков не поддерживает более двух проходов. настройте DMO для использования двух проходов, задав для [свойства \_ пассесусед мфпкэй](mfpkey-passesusedproperty.md) значение 2.

доставьте образцы в кодировщик DMO по одному за раз, как в однопроходном режиме. При обработке входных примеров для этапа предварительной обработки вызовы [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) или [**Имфтрансформ::P Роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) возвратит **\_ значение S false**, чтобы указать, что выходные данные не создаются.

В конце первого прохода (после первой обработки последнего ввода) необходимо задать свойство [мфпкэй \_ ендофпасс](mfpkey-endofpassproperty.md) , чтобы уведомить кодек о том, что следующий обработанный ввод является первым входом второго прохода. Для этого свойства значение не требуется, поэтому следует использовать пустую структуру **Variant** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Кодеки Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
