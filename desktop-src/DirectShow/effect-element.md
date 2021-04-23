---
description: Элемент Effect определяет объект аудио или видео. Результат применяется к одному потоку (например, композиции, дорожке или источнику).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Элемент Effect (Гдиплусеффектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908662"
---
# <a name="effect-element"></a>Элемент Effect

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`effect`Элемент определяет объект аудио или видео. Результат применяется к одному потоку (например, композиции, дорожке или источнику).

## <a name="attributes"></a>Атрибуты

[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**выкл**](mute-attribute.md)., [**Запуск**](start-attribute.md), [**Завершение**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



| Метка | Значение |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Parent   | [**составной**](composite-element.md), [**Группа**](group-element.md), [**Обрезка**](clip-element.md), [**запись**](track-element.md) |
| Дети | [**param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Комментарии

Атрибут **CLSID** задает подобъект, который создает результат.

## <a name="examples"></a>Примеры


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Гдиплусеффектс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 




