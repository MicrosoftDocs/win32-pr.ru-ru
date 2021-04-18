---
title: Метод Media. Жетмаркернаме
description: Метод Жетмаркернаме извлекает имя маркера по указанному индексу.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- Жетмаркернаме метод Windows Media Player
- Жетмаркернаме метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетмаркернаме
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699094"
---
# <a name="mediagetmarkername-method"></a>Метод Media. Жетмаркернаме

Метод **жетмаркернаме** извлекает имя маркера по указанному индексу.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*маркернум* \[ окне\]
</dt> <dd>

**Число** (**длинное**), определяющее индекс маркера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Комментарии

Этот метод возвращает **значение NULL** , если указанный маркер не существует.

Некоторые цифровые мультимедийные элементы не содержат маркеров. Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем клипе.

Номера индексов маркеров начинаются с 1.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *носитель*. **жетмаркернаме** для заполнения HTML-элемента textarea с именем мнамес именами маркеров в текущем элементе мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
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

[**Media. Жетмаркертиме**](media-getmarkertime.md)
</dt> <dt>

[**Media. Маркеркаунт**](media-markercount.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





