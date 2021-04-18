---
description: Загрузка последовательности символов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: 'ID3DX10Font: метод:P Релоадчарактерс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664977"
---
# <a name="id3dx10fontpreloadcharacters-method"></a>ID3DX10Font: метод:P Релоадчарактерс

Загрузка последовательности символов в видеопамять для повышения эффективности отрисовки на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сначала* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор первого символа, загружаемого в видеопамять.

</dd> <dt>

*Последний раз* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор последнего символа, который должен быть загружен в видеопамять.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Комментарии

Этот метод создает текстуры, содержащие глифы, представляющие входные символы. Глифы рисуются в виде ряда треугольников.

Символы не будут подготавливаться к просмотру на устройстве; ID3DX10Font: для отрисовки символов необходимо по-прежнему вызывать метод:D Равтекст. Однако предварительная загрузка символов в видеопамять ID3DX10Font::D Равтекст будет использовать значительно меньше ресурсов ЦП.

Этот метод внутренне преобразует символы в глифы с помощью функции GDI [жетчарактерплацемент](/previous-versions//ms534004(v=vs.85)).

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

 

 
