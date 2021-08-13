---
title: Медиаколлектион. Жетстрингколлектионбикуери, метод
description: Метод Жетстрингколлектионбикуери извлекает объект StringCollection, содержащий все строки, соответствующие условиям запроса.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- проигрыватель Windows Media метода жетстрингколлектионбикуери
- проигрыватель Windows Media метода жетстрингколлектионбикуери, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод жетстрингколлектионбикуери
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
ms.openlocfilehash: 6d9e8f2eae2ce52a566d4db6b8298187df1d4d444432e99dda22d3cacc0ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390114"
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

## <a name="remarks"></a>Remarks

В составных запросах, использующих **запрос** , регистр не учитывается.

Если составной запрос, заданный параметром *запроса* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется. Значение параметра *mediaType* всегда используется. Например, если составной запрос содержит условие «MediaType равно Audio», а параметру *mediaType* — «Video», то итоговый список будет содержать только элементы видео.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Атрибут MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Объект запроса**](query-object.md)
</dt> </dl>

 

 





