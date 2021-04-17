---
title: Метод Media. Жетмаркертиме
description: Метод Жетмаркертиме извлекает время маркера по указанному индексу.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- Жетмаркертиме метод Windows Media Player
- Жетмаркертиме метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетмаркертиме
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699006"
---
# <a name="mediagetmarkertime-method"></a>Метод Media. Жетмаркертиме

Метод **жетмаркертиме** извлекает время маркера по указанному индексу.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*маркернум* \[ окне\]
</dt> <dd>

**Число** (**длинное**), указывающее индекс маркера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Double**), задающее положение маркера в секундах от начала клипа.

## <a name="remarks"></a>Комментарии

Этот метод возвращает **значение NULL** , если указанный маркер не существует.

Некоторые цифровые мультимедийные элементы не содержат маркеров. Используйте **маркеркаунт** , чтобы узнать, сколько маркеров находится в текущем клипе.

Номера индексов маркеров начинаются с 1.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *носитель*. **жетмаркертиме** для заполнения HTML-элемента textarea с именем мтимес расположением каждого маркера. Объект **Player** создан с идентификатором "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
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

[**Media. Жетмаркернаме**](media-getmarkername.md)
</dt> <dt>

[**Media. Маркеркаунт**](media-markercount.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





