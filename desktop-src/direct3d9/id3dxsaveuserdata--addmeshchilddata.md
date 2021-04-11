---
description: Добавление дочерних данных в сетку.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'Метод ID3DXSaveUserData:: Аддмешчилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273949"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>Метод ID3DXSaveUserData:: Аддмешчилддата

Добавление дочерних данных в сетку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмешконтаинер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Указатель на контейнер сетки. См. [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*пксофсаве* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Указатель на файл. x сохранить объект. Используйте указатель для вызова [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md) , чтобы добавить дочерний объект данных. Не сохраняйте данные с помощью [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*пксофмешдата* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Указатель на узел данных файла. x. Используйте указатель для вызова [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) , чтобы добавить дочерний объект данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
