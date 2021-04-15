---
title: IWMPMediaCollection2 Жетплайлистбикуери, метод
description: Метод Жетплайлистбикуери возвращает интерфейс Ивмпплайлист, который предоставляет доступ к элементам мультимедиа, соответствующим условиям запроса.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Жетплайлистбикуери метод Windows Media Player
- Жетплайлистбикуери метод проигрывателя Windows Media Player, интерфейс IWMPMediaCollection2
- Интерфейс IWMPMediaCollection2 Windows Media Player, метод Жетплайлистбикуери
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648797"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>Метод IWMPMediaCollection2:: Жетплайлистбикуери

`getPlaylistByQuery`Метод возвращает интерфейс **ивмпплайлист** , который предоставляет доступ к элементам мультимедиа, соответствующим условиям запроса.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуери* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпкуери** , представляющий запрос.

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

Значение **System. Boolean** , указывающее, должен ли список воспроизведения быть отсортирован в возрастающем порядке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпплайлист** для полученного списка воспроизведения.

## <a name="remarks"></a>Комментарии

В составных запросах, использующих **ивмпкуери** , регистр не учитывается.

Если составной запрос, заданный параметром *пкуери* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется. Значение параметра *бстрмедиатипе* всегда используется. Например, если составной запрос содержит условие «MediaType равно Audio», а значение параметра *бстрмедиатипе* — «Video», то итоговый список будет содержать только элементы видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPMediaCollection2 (VB и C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкуери (VB и C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Атрибут MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





