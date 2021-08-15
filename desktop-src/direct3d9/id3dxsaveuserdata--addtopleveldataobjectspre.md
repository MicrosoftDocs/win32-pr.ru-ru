---
description: Добавьте объект верхнего уровня перед иерархией Frame.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'Метод ID3DXSaveUserData:: Аддтоплевелдатаобжектспре (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52052a24c34c99260a68cd5cdeaa7487e6b71c086ac30922a06de241de8319ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801169"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>Метод ID3DXSaveUserData:: Аддтоплевелдатаобжектспре

Добавьте объект верхнего уровня перед иерархией Frame.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddTopLevelDataObjectsPre(
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
