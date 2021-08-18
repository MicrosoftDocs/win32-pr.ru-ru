---
title: EFFECTs. Куррентеффект
description: Атрибут Куррентеффект указывает или получает текущую визуализацию.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- effects. куррентеффект проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9ac47ef88d1a0bce4982f71ce2e20e33f48933c9916bbb1e62085b5a1e5178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996874"
---
# <a name="effectscurrenteffect"></a>EFFECTs. Куррентеффект

Атрибут **куррентеффект** указывает или получает текущую визуализацию.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **объектом**, предназначенным для чтения и записи. Значение по умолчанию — первое визуализация в порядке создания. Если в обложке нет созданных визуализаций, по умолчанию используется первая визуализация в реестре.

## <a name="remarks"></a>Remarks

Этот объект можно использовать для доступа к пользовательским визуализациям, которые вы создали. Например, можно предоставить свойство через интерфейс **IDispatch** в визуализации. Затем можно изменить значение свойства из обложки, сделав визуализацию текущим, а затем используя объект **куррентеффект** , чтобы задать новое значение для свойства. например, если визуализация предоставляет свойство с именем backgroundColor, в следующем JScript коде указывается новое значение:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EFFECTs, элемент**](effects-element.md)
</dt> <dt>

[**EFFECTs. Куррентеффекттитле**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTs. Куррентеффекттипе**](effects-currenteffecttype.md)
</dt> </dl>

 

 





