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
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354763"
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

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет тип структуры. Если определен Юникод, функция возвращает структуру ТЕКСТМЕТРИКВ. В противном случае вызов функции возвращает структуру ТЕКСТМЕТРИКА.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
