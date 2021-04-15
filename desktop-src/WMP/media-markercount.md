---
title: Media. Маркеркаунт
description: Свойство Маркеркаунт извлекает количество маркеров в элементе мультимедиа.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. Маркеркаунт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695151"
---
# <a name="mediamarkercount"></a>Media. Маркеркаунт

Свойство **маркеркаунт** извлекает количество маркеров в элементе мультимедиа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. **маркеркаунт**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное**), определяющим количество маркеров в файле.

## <a name="remarks"></a>Комментарии

Это свойство возвращает нуль, если файл не имеет маркеров, или если элемент мультимедиа не совпадает с *проигрывателем*. **куррентмедиа**.

Номера маркеров начинаются с 1.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *носитель*. **маркеркаунт** для получения количества маркеров в текущем элементе мультимедиа. Это значение затем используется в качестве верхней границы для циклической структуры, которая выполняет итерацию по списку маркеров для получения каждого имени маркера. Элемент TEXTAREA HTML с именем МНАМЕС отображает имена маркеров в текущем элементе мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Player. Куррентмедиа**](player-currentmedia.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





