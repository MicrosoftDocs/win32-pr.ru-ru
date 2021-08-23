---
description: Получение характеристик шрифта.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'Метод ID3DX10Font:: Жеттекстметрикс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047052"
---
# <a name="id3dx10fontgettextmetrics-method"></a>Метод ID3DX10Font:: Жеттекстметрикс

Получение характеристик шрифта.

## <a name="syntax"></a>Синтаксис


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстметрикс* \[ окне\]
</dt> <dd>

Тип: **текстметрик \***

Указатель на структуру [текстметрик](/previous-versions//ms534202(v=vs.85)) , которая содержит свойства шрифта. Если определен Юникод, функция возвращает структуру ТЕКСТМЕТРИКВ. В противном случае функция возвращает структуру ТЕКСТМЕТРИКА.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Ненулевое значение, если функция выполнена успешно; в противном случае — 0.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
