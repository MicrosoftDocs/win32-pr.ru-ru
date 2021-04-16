---
title: ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет
description: Метод Некстпресет применяет следующую предустановку эквалайзера.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699143"
---
# <a name="equalizersettingsnextpreset"></a>ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет

Метод **некстпресет** применяет следующую предустановку эквалайзера.

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если текущая Предустановка является последней доступной, первая Предустановка становится текущей.

## <a name="examples"></a>Примеры


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Превиауспресет**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





