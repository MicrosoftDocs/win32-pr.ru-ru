---
title: IWMPMediaCollection2 Жетстрингколлектионбикуери, метод
description: Метод Жетстрингколлектионбикуери возвращает интерфейс Ивмпстрингколлектион, который предоставляет доступ к набору всех строковых значений для указанного атрибута, соответствующих условиям запроса.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- проигрыватель Windows Media метода жетстрингколлектионбикуери
- проигрыватель Windows Media метода жетстрингколлектионбикуери, интерфейс IWMPMediaCollection2
- проигрыватель Windows Media интерфейса IWMPMediaCollection2, метод жетстрингколлектионбикуери
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054dd5b76cb6dcf3e6cb29ba624cd1f5c0f281d69c4b2b5e5125f5de9b4e7b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745972"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>Метод IWMPMediaCollection2:: Жетстрингколлектионбикуери

`getStringCollectionByQuery`Метод возвращает интерфейс **ивмпстрингколлектион** , который предоставляет доступ к набору всех строковых значений для указанного атрибута, соответствующих условиям запроса.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраттрибуте* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута.

</dd> <dt>

*пкуери* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпкуери** , который представляет собой запрос, определяющий условия, используемые для получения коллекции строк.

</dd> <dt>

*бстрмедиатипе* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является типом мультимедиа. Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".

</dd> <dt>

*бстрсортаттрибуте* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута, используемого для сортировки. Строка нулевой длины ("") означает, что сортировка не применяется.

</dd> <dt>

*фсортасцендинг* \[ окне\]
</dt> <dd>

Значение **System. Boolean** , указывающее, должен ли набор строковых значений быть отсортирован в возрастающем порядке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпстрингколлектион** для полученного набора строковых значений.

## <a name="remarks"></a>Remarks

В составных запросах, использующих **ивмпкуери** , регистр не учитывается.

Если составной запрос, заданный параметром *пкуери* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется. Значение параметра *бстрмедиатипе* всегда используется. Например, если составной запрос содержит условие «MediaType равно Audio», а значение параметра *бстрмедиатипе* — «Video», то итоговый список будет содержать только элементы видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPMediaCollection2 (VB и C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкуери (VB и C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпстрингколлектион (VB и C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Атрибут MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





