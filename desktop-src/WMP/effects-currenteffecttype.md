---
title: EFFECTs. Куррентеффекттипе
description: Атрибут Куррентеффекттипе указывает или получает имя реестра текущей визуализации. Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- Effect. Куррентеффекттипе Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694708"
---
# <a name="effectscurrenteffecttype"></a>EFFECTs. Куррентеффекттипе

Атрибут **куррентеффекттипе** указывает или получает имя реестра текущей визуализации. Это имя является уникальным ИДЕНТИФИКАТОРом, определенным автором визуализации.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Этот атрибут можно использовать во время выполнения, чтобы изменить отображаемый в данный момент результат. Для этого выполните следующие действия.

1.  Используйте **еффекткаунт** для получения числа зарегистрированных эффектов.
2.  В цикле извлеките имя каждого зарегистрированного результата с помощью **еффекттипе**.
3.  Укажите одно из имен, полученных для **куррентеффекттипе** , чтобы установить текущий результат.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EFFECTs, элемент**](effects-element.md)
</dt> <dt>

[**EFFECTs. Куррентеффект**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTs. Еффекткаунт**](effects-effectcount.md)
</dt> <dt>

[**EFFECTs. Еффекттипе**](effects-effecttype.md)
</dt> </dl>

 

 





