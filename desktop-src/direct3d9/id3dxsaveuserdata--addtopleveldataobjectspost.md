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
ms.openlocfilehash: cd0d631a814b25e8ff99272a29af377941e2a6865bd41e6a2fb2c6bcc8fc59a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727824"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
