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
ms.openlocfilehash: c2989ce2a662be5a1ec53c961b8fafa072862fc2b43b6003b04f6b887ef3c077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790544"
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

## <a name="remarks"></a>Remarks

Методы ID3DXPRTEngine:: Компутекскскс вычисляют выходные буферы, в которых сигнал освещения не умножается на албедо. Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.

Чтобы включить албедо в модель, подготовленную к просмотру, вызовите этот метод после одного из методов Компутекскскс.

Перед вызовом этого метода необходимо вызвать [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Компутедиректлигхтингш**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




