---
description: Получение описания текущего объекта Font.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'Метод ID3DX10Font:: desc (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664991"
---
# <a name="id3dx10fontgetdesc-method"></a>Метод ID3DX10Font:: DESC

Получение описания текущего объекта Font.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдеск* \[ окне\]
</dt> <dd>

Тип: **[ **D3DX10 \_ Font \_ DESC**](d3dx10-font-desc.md)\***

Указатель на [**D3DX10 структуру \_ шрифта \_**](d3dx10-font-desc.md) , описывающую объект Font. Если определен Юникод, возвращается указатель на D3DX10FONT \_ дескв; в противном случае возвращается указатель на D3DX10FONT \_ DESC.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод описывает объекты шрифтов Юникода, если задан Юникод. В противном случае вызывается метод-DESC, который возвращает указатель на \_ структуру D3DX10FONT DESC.

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

 

 




