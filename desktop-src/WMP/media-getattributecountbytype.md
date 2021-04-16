---
title: Метод Media. Жетаттрибутекаунтбитипе
description: Метод Жетаттрибутекаунтбитипе извлекает количество атрибутов, связанных с указанным именем атрибута и языком.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Жетаттрибутекаунтбитипе метод Windows Media Player
- Жетаттрибутекаунтбитипе метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод Жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699099"
---
# <a name="mediagetattributecountbytype-method"></a>Метод Media. Жетаттрибутекаунтбитипе

Метод **жетаттрибутекаунтбитипе** извлекает количество атрибутов, связанных с указанным именем атрибута и языком.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> <dt>

*языковая* \[ окне\]
</dt> <dd>

**Строка** , представляющая язык. Если задано значение null или "" (пустая строка), используется текущая строка языкового стандарта. В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**), содержащее число атрибутов.

## <a name="remarks"></a>Комментарии

Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для данного объекта **мультимедиа** . Номера индексов можно передать в метод **жетитеминфобитипе** . Это полезно, например, когда элемент мультимедиа был разбит на несколько жанров.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**медиаобжект**](media-object.md)
</dt> <dt>

[**Media. Жетитеминфобитипе**](media-getiteminfobytype.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





