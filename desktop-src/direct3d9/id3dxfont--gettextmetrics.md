---
description: Получает характеристики шрифта, определенные в структуре ТЕКСТМЕТРИК. Этот метод поддерживает параметры компилятора ANSI и Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'Метод ID3DXFont:: Жеттекстметрикс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9254ec9d5224f9041079f36bc95d68ea7346cf6dac2aecb81e7a6009496675e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987414"
---
# <a name="id3dxfontgettextmetrics-method"></a>Метод ID3DXFont:: Жеттекстметрикс

Получает характеристики шрифта, определенные в структуре [**текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Этот метод поддерживает параметры компилятора ANSI и Unicode.

## <a name="syntax"></a>Синтаксис


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстметрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Указатель на структуру [**текстметрик**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , которая содержит свойства шрифта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Ненулевое значение, если функция выполнена успешно; в противном случае — 0.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет тип структуры. Если определен Юникод, функция возвращает структуру ТЕКСТМЕТРИКВ. В противном случае вызов функции возвращает структуру ТЕКСТМЕТРИКА.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
