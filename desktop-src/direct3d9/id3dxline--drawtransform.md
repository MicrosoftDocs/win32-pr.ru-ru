---
description: Рисует полосу линий в пространстве экрана с заданной матрицей преобразования входных данных.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: 'ID3DXLine: метод:D Равтрансформ (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694283"
---
# <a name="id3dxlinedrawtransform-method"></a>ID3DXLine: метод:D Равтрансформ

Рисует полосу линий в пространстве экрана с заданной матрицей преобразования входных данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвертекслист* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Массив вершин, образующих линию. См. [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*дввертекслисткаунт* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число вершин в списке вершин.

</dd> <dt>

*птрансформ* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Матрица масштабирования, вращения и сдвига (SRT) для преобразования точек. См. [**D3DXMATRIX**](d3dxmatrix.md). Если эта матрица является матрицей проекции, то все стипплед линии будут отображаться с шаблоном стипплинг с перспективой. Также можно преобразовать вершины и использовать [**ID3DXLine::D RAW**](id3dxline--draw.md) , чтобы нарисовать линию с неправильным шаблоном стиппле.

</dd> <dt>

*Цветовая палитра* \[ окне\]
</dt> <dd>

Тип: **[ **D3DCOLOR**](d3dcolor.md)**

Цвет линии. См. [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
