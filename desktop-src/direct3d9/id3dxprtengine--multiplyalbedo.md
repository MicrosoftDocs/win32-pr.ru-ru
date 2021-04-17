---
description: Умножает каждый предварительно вычисленный вектор радианценой пересылки (PRT) на вершину албедо.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'Метод ID3DXPRTEngine:: Мултиплялбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703955"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>Метод ID3DXPRTEngine:: Мултиплялбедо

Умножает каждый предварительно вычисленный вектор радианценой пересылки (PRT) на вершину албедо.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который будет содержать ВЕКТОРы PRT, умноженные на албедо вершины. Если этот выходной буфер является объектом текстуры, необходимо соблюдать осторожность, чтобы сохранить албедо текстуры в том же разрешении, что и буфер имитации. Вы можете задать правильное разрешение для албедо с [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), применяя области для переплета текстур, если это уместно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Методы ID3DXPRTEngine:: Компутекскскс вычисляют выходные буферы, в которых сигнал освещения не умножается на албедо. Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.

Чтобы включить албедо в модель, подготовленную к просмотру, вызовите этот метод после одного из методов Компутекскскс.

Перед вызовом этого метода необходимо вызвать [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутедиректлигхтингш**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




