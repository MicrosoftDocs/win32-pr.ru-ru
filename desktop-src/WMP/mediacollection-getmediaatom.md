---
title: Медиаколлектион. Жетмедиаатом, метод
description: Метод Жетмедиаатом извлекает индекс, по которому указанный атрибут находится в наборе доступных атрибутов.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- проигрыватель Windows Media метода жетмедиаатом
- проигрыватель Windows Media метода жетмедиаатом, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод жетмедиаатом
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f537b759516d5fa0f382d0c72aabbc0edb836ad8e4ae6d7f210d012fa19ea60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837207"
---
# <a name="mediacollectiongetmediaatom-method"></a>Медиаколлектион. Жетмедиаатом, метод

Метод **жетмедиаатом** извлекает индекс, по которому указанный атрибут находится в наборе доступных атрибутов.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибуту](attribute-reference.md)проигрыватель Windows Media.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**).

## <a name="remarks"></a>Remarks

Номер индекса, полученный с помощью этого метода, может быть передан на *носитель*. метод **жетитеминфобятом** для доступа к значениям атрибутов. Эта методика обычно более эффективна при работе с большими списками воспроизведения, чем доступ к значению атрибута по имени через *носитель*. **getItemInfo** или *Media*. **жетитеминфобитипе**.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. Жетитеминфобятом**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media. Жетитеминфобитипе**](media-getiteminfobytype.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





