---
description: Добавьте объект верхнего уровня после иерархии Frame.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'Метод ID3DXSaveUserData:: Аддтоплевелдатаобжектспост (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081938"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>Метод ID3DXSaveUserData:: Аддтоплевелдатаобжектспост

Добавьте объект верхнего уровня после иерархии Frame.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пксофсаве* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Указатель на файл. x сохранить объект. Используйте этот указатель для вызова [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект данных для сохранения. Затем вызовите метод [**идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md) , чтобы сохранить данные.

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

 

 
