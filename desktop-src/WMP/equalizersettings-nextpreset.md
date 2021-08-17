---
title: ЕКУАЛИЗЕРСЕТТИНГС. Некстпресет
description: Метод Некстпресет применяет следующую предустановку эквалайзера.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- екуализерсеттингс. некстпресет проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 715c5ee514cf2818cbab8b5553cab9565a2b448e47d1f6fe2282f17940cfc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748699"
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

## <a name="remarks"></a>Remarks

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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. Превиауспресет**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





