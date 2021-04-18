---
title: Controls. Куррентмаркер
description: Свойство Куррентмаркер указывает или получает номер текущего маркера.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Проигрыватель Windows Media Controls. Куррентмаркер
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698790"
---
# <a name="controlscurrentmarker"></a>Controls. Куррентмаркер

Свойство **куррентмаркер** указывает или получает номер текущего маркера.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство имеет **номер** для чтения и записи (**Long**) и значение по умолчанию 0.

## <a name="remarks"></a>Комментарии

Установка **куррентмаркер** приводит к запуску воспроизведения с указанного маркера. Прежде чем приступить к установке **куррентмаркер**, определите, есть ли у файла маркеры и сколько он имеет с помощью **маркеркаунт**. Если у файла нет маркеров, установка **куррентмаркер** в любом случае, но ноль приводит к ошибке. Установка **куррентмаркер** в число, превышающее **маркеркаунт** , также приводит к ошибке.

Свойство **куррентмаркер** всегда возвращает текущий или последний маркер, то есть фактическое расположение файла может находиться либо на текущем маркере, либо перед следующим маркером. Маркеры нумеруются, начиная с 1, поэтому если в файле есть маркеры, можно установить **куррентмаркер** в ноль, чтобы изменить расположение файла на ноль.

До тех пор, пока не будет задан текущий элемент мультимедиа (с помощью *проигрывателя*.**URL-адрес** или *проигрыватель*. **куррентмедиа**), **куррентмаркер** возвращает ноль.

## <a name="examples"></a>Примеры

В следующем примере JScript используется **куррентмаркер** для запуска воспроизведения видео из маркера, соответствующего свойству **SelectedIndex** HTML-элемента SELECT. Объект **Player** создан с идентификатором "Player".


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Media. Маркеркаунт**](media-markercount.md)
</dt> <dt>

[**Player. Куррентмедиа**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





