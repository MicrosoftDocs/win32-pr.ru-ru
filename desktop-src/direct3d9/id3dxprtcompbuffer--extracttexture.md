---
description: Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных ID3DXPRTCompBuffer и добавляет их в объект IDirect3DTexture9.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'Метод ID3DXPRTCompBuffer:: Екстракттекстуре (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081890"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a>Метод ID3DXPRTCompBuffer:: Екстракттекстуре

Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) и добавляет их в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стартпка* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Начальное значение коэффициента буфера, из которого извлекаются данные текстуры.

</dd> <dt>

*Нумпка* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество коэффициентов PCA для извлечения из буфера.

</dd> <dt>

*птекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на объект текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , в котором будут храниться коэффициенты PCA.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
