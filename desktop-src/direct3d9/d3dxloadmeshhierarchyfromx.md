---
description: Загружает первую иерархию кадров из файла. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Функция D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000313"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>Функция D3DXLoadMeshHierarchyFromX

Загружает первую иерархию кадров из файла. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

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

*ппфрамехиерарчи* \[ заполняет\]
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

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXLoadMeshHierarchyFromXW. В противном случае вызов функции разрешается в D3DXLoadMeshHierarchyFromXA.

Все сетки в файле будут свернуты в одну выходную сетку. Если файл содержит иерархию рамок, все преобразования будут применены к сетке.

**D3DXLoadMeshHierarchyFromX** загружает данные анимации и иерархию кадров из файла. x. Он сканирует файл x и строит иерархию кадров и контроллер анимации в соответствии с объектом, производным от [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), который передается в него через паллок. Для загрузки данных необходимо выполнить следующие действия.

1.  Производные [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), реализующие каждый метод. Это определяет, как выделяются и освобождаются фреймы и сетки.
2.  Производные [**ID3DXLoadUserData**](id3dxloaduserdata.md), реализующие каждый метод. Если файл. x не содержит внедренных пользовательских данных или его не требуется, можно пропустить эту часть.
3.  Создайте объект класса [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) и, при необходимости, класс лоадусердата. Нет необходимости самостоятельно вызывать методы этих объектов.
4.  Вызовите **D3DXLoadMeshHierarchyFromX**, передав объект [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) и объект [**ID3DXLoadUserData**](id3dxloaduserdata.md) (или **значение NULL**), чтобы создать иерархию кадров и контроллер анимации. Все наборы и кадры анимации автоматически регистрируются в контроллере анимации.

Во время загрузки [**креатефраме**](id3dxallocatehierarchy--createframe.md) и [**лоадфрамечилддата**](id3dxloaduserdata--loadframechilddata.md) вызываются обратно в каждом кадре для управления загрузкой и выделением кадра. Приложение определяет эти методы для управления сохранением кадров. [**Креатемешконтаинер**](id3dxallocatehierarchy--createmeshcontainer.md) и [**лоадмешчилддата**](id3dxloaduserdata--loadmeshchilddata.md) вызываются обратно для каждого объекта сетки, чтобы управлять загрузкой и выделением объектов сетки. [**Лоадтоплевелдата**](id3dxloaduserdata--loadtopleveldata.md) вызывается обратно для каждого объекта верхнего уровня, который не загружается другими методами.

Чтобы освободить эти данные, вызовите ID3DXAnimationController:: Release, чтобы освободить наборы анимации, и [**D3DXFRAMEDestroy**](d3dxframedestroy.md), передав корневой узел иерархии Frame и объект производного класса [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) . [**Дестройфраме**](id3dxallocatehierarchy--destroyframe.md) и [**дестроймешконтаинер**](id3dxallocatehierarchy--destroymeshcontainer.md) будут вызываться для каждого объекта Frame и сетки в иерархии Frame. Ваша реализация **дестройфраме** должна освободить все, что выделено [**креатефраме**](id3dxallocatehierarchy--createframe.md), а также методы контейнера сетки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
