---
description: Возвращает описание текущего объекта Font. Жетдескв и DESC идентичны этому методу, за исключением того, что указатель возвращается в \_ структуру D3DXFONT дескв или D3DXFONT \_ DESC соответственно.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'Метод ID3DXFont:: desc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2961c69e47bb46eaf782e8f5d4dbfe0be2d82a49f00f98c36b1ee7b141e962b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675434"
---
# <a name="id3dxfontgetdesc-method"></a>Метод ID3DXFont:: DESC

Возвращает описание текущего объекта Font. Жетдескв и DESC идентичны этому методу, за исключением того, что указатель возвращается в структуру [**D3DXFONT \_ Дескв**](d3dxfont-desc.md) или **D3DXFONT \_ DESC** соответственно.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

Указатель на структуру [**D3DXFONT \_ DESC**](d3dxfont-desc.md) , описывающую объект Font.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Этот метод описывает объекты шрифтов Юникода, если задан Юникод. В противном случае вызывается метод-DESC, который возвращает указатель на структуру [**D3DXFONT \_ DESC**](d3dxfont-desc.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




