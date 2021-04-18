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
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547943"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
