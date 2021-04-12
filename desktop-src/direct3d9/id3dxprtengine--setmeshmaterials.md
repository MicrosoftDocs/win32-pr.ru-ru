---
description: Задает свойства материала сетки в трехмерной сцене. Используйте этот метод, чтобы указать параметры геоточечной подповерхности.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'Метод ID3DXPRTEngine:: Сетмешматериалс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355683"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>Метод ID3DXPRTEngine:: Сетмешматериалс

Задает свойства материала сетки в трехмерной сцене. Используйте этот метод, чтобы указать параметры геоточечной подповерхности.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппматериалс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Адрес указателя на требуемые свойства материала сетки. См. [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*Нуммешес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс сетки, для которой задаются свойства материала.

</dd> <dt>

*Нумчаннелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число цветовых каналов, устанавливаемых в сетке. Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные. Если вы собираетесь изменить этот параметр, сначала установите албедо с помощью другого метода, такого как [**ID3DXPRTEngine:: сетпертекселалбедо**](id3dxprtengine--setpertexelalbedo.md) или [**ID3DXPRTEngine:: сетпервертексалбедо**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*бсеталбедо* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение — true**, задает для албедо сетки значение ппматериалс, перезаписывая все существующие значения шаг текселя и вершин албедо. Если **значение равно false**, сохраняет все существующие значения шаг текселя и вершин албедо, заданные другими методами. Нумчаннелс должен соответствовать параметру Нумчаннелс, используемому для создания буфера в [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) или [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).

</dd> <dt>

*фленгсскале* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Масштаб трехмерной сцены относительно Куба 1 мм. Используется для вычислений с разбросами подповерхности.

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

 

 
