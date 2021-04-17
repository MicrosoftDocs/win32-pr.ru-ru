---
title: Медиаколлектион. Жетстрингколлектионбикуери, метод
description: Метод Жетстрингколлектионбикуери извлекает объект StringCollection, содержащий все строки, соответствующие условиям запроса.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Жетстрингколлектионбикуери метод Windows Media Player
- Жетстрингколлектионбикуери метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетстрингколлектионбикуери
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685412"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>Медиаколлектион. Жетстрингколлектионбикуери, метод

Метод **жетстрингколлектионбикуери** извлекает объект **StringCollection** , содержащий все строки, соответствующие условиям запроса.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута.

</dd> <dt>

*запрос* \[ окне\]
</dt> <dd>

Объект **запроса** .

</dd> <dt>

*mediaType* \[ окне\]
</dt> <dd>

**Строка** , содержащая тип носителя. Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".

</dd> <dt>

*sortAttribute* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута, используемого для сортировки. Пустая строка ("") означает, что сортировка не применяется.

</dd> <dt>

*сортасцендинг* \[ окне\]
</dt> <dd>

**Логическое** значение, true, указывающее, что **StringCollection** должен быть отсортирован в возрастающем порядке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **StringCollection** .

## <a name="remarks"></a>Комментарии

В составных запросах, использующих **запрос** , регистр не учитывается.

Если составной запрос, заданный параметром *запроса* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется. Значение параметра *mediaType* всегда используется. Например, если составной запрос содержит условие «MediaType равно Audio», а параметру *mediaType* — «Video», то итоговый список будет содержать только элементы видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Атрибут MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Объект запроса**](query-object.md)
</dt> </dl>

 

 





