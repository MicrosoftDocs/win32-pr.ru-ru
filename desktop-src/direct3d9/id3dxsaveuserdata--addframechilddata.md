---
description: Добавьте дочерние данные в рамку.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'Метод ID3DXSaveUserData:: Аддфрамечилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0b593010ec9ff8a56833c48b9667dfd0084f99283fc4bf29c9008e9e31ac98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095724"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a>Метод ID3DXSaveUserData:: Аддфрамечилддата

Добавьте дочерние данные в рамку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфраме* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFRAME**](d3dxframe.md) \***

Указатель на контейнер сетки. См. [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*пксофсаве* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Указатель на файл. x сохранить объект. Используйте указатель для вызова [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md) , чтобы добавить дочерний объект данных. Не сохраняйте данные с помощью [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*пксоффрамедата* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Указатель на узел данных файла. x. Используйте указатель для вызова [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) , чтобы добавить дочерний объект данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.

## <a name="remarks"></a>Remarks

[**ID3DXSaveUserData:: регистертемплатес**](id3dxsaveuserdata--registertemplates.md) и [**ID3DXSaveUserData:: саветемплатес**](id3dxsaveuserdata--savetemplates.md) предоставляют механизм для добавления шаблона в файл. x для сохранения пользовательских данных.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
