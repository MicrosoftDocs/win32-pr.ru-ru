---
title: Элемент DURATION
description: Элемент DURATION определяет продолжительность времени, в течение которого проигрыватель Windows Media выводит связанную запись списка воспроизведения.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Элемент DURATION проигрыватель Windows Media
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698981"
---
# <a name="duration-element"></a>Элемент DURATION

Элемент **DURATION** определяет продолжительность времени, в течение которого проигрыватель Windows Media выводит связанную запись списка воспроизведения.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Атрибуты

**Значение** (обязательно)

Продолжительность времени в часах, минутах, секундах и сотых долях секунды, которая отрисовывается проигрывателем Windows Media. Значение по умолчанию — это вся длина записи. Если запись является графическим файлом, необходимо указать значение длительности.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы           |
|-----------------|--------------------|
| Родительские элементы | **entry**, **ref** |
| Дочерние элементы  | Нет               |



 

## <a name="remarks"></a>Remarks

Этот элемент определяет продолжительность времени, в течение которого поток должен быть визуализирован. Если **значение атрибута value** превышает длину потока содержимого, поток завершается в его нормальной конечной точке.

Этот элемент может находиться либо в элементе **ref** , либо в элементе **entry** . Однако элемент **DURATION** , определенный в элементе **ref** , переопределяет тот, который отображается в родительском элементе **entry** элемента **ref** .

Элемент **DURATION** переопределяет элемент **превиевдуратион** .

## <a name="examples"></a>Примеры


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Справочник по метафайлу Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





