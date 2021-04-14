---
description: Задает стандартный вектор для каждого шаг текселя в объекте текстуры. Этот метод используется для хранения векторов нормали вершин из сетки (или интерполяции нормалей вершин, если выполняется вычисление предварительно вычисленных радианце передаваемых данных (PRT) на основе пикселя).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'Метод ID3DXPRTEngine:: Сетпертекселнормал (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424433"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>Метод ID3DXPRTEngine:: Сетпертекселнормал

Задает стандартный вектор для каждого шаг текселя в объекте текстуры. Этот метод используется для хранения векторов нормали вершин из сетки (или интерполяции нормалей вершин, если выполняется вычисление предварительно вычисленных радианце передаваемых данных (PRT) на основе пикселя).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнормалтекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на объект текстуры [**IDirect3DTexture9**](/windows/desktop/api) , который служит в качестве стандартной схемы пространства объектов для хранения обычных векторов. Текстура должна иметь те же размеры, что и [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , и должна иметь возможность хранить подписанные форматы текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
