---
description: Функция D3DXLoadMeshHierarchyFromXInMemory — загружает первую иерархию кадров из файла. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Функция D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098212"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>Функция D3DXLoadMeshHierarchyFromXInMemory

Загружает первую иерархию кадров из файла. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмемори* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на буфер, содержащий иерархию сетки.

</dd> <dt>

*Сизеофмемори* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Размер буфера Пмемори в байтах.

</dd> <dt>

*Мешоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , задающих параметры создания для сетки.

</dd> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.

</dd> <dt>

*паллок* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Указатель на интерфейс [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*пусердаталоадер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Предоставленный приложением интерфейс, позволяющий загружать пользовательские данные. См. [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ппфрамехеирарчи* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Возвращает указатель на иерархию загруженных кадров. См. [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ппанимконтроллер* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Возвращает указатель на контроллер анимации, соответствующий анимации в файле. x. Он создается с отслеживанием и событиями по умолчанию. См. [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Все сетки в файле будут свернуты в одну выходную сетку. Если файл содержит иерархию рамок, все преобразования будут применены к сетке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
