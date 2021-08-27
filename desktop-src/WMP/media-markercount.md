---
title: Media. Маркеркаунт
description: Свойство Маркеркаунт извлекает количество маркеров в элементе мультимедиа.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- проигрыватель Windows Media Media. маркеркаунт
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
ms.openlocfilehash: 00206991f81c6a445648a063a37bcc45bf91f647b60317772478142eefd1b20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123354"
---
# <a name="mediamarkercount"></a>Media. Маркеркаунт

Свойство **маркеркаунт** извлекает количество маркеров в элементе мультимедиа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. **маркеркаунт**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное**), определяющим количество маркеров в файле.

## <a name="remarks"></a>Remarks

Это свойство возвращает нуль, если файл не имеет маркеров, или если элемент мультимедиа не совпадает с *проигрывателем*. **куррентмедиа**.

Номера маркеров начинаются с 1.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **маркеркаунт** для получения количества маркеров в текущем элементе мультимедиа. Это значение затем используется в качестве верхней границы для циклической структуры, которая выполняет итерацию по списку маркеров для получения каждого имени маркера. Элемент TEXTAREA HTML с именем МНАМЕС отображает имена маркеров в текущем элементе мультимедиа. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Player. Куррентмедиа**](player-currentmedia.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





