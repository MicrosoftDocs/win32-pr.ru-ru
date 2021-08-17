---
description: Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'Метод ID3DXSaveUserData:: Регистертемплатес (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a41a43f8f319ee09f24c4f62092e4718773dc312cb7886b0fc7c95781e614c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628734"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>Метод ID3DXSaveUserData:: Регистертемплатес

Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пксфилеапи* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFILE**](id3dxfile.md)**

Этот указатель используется для регистрации определяемых пользователем шаблонов файлов x. См. [**ID3DXFile**](id3dxfile.md). Не используйте этот параметр для добавления объектов данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.

## <a name="remarks"></a>Remarks

**ID3DXSaveUserData:: регистертемплатес** и [**ID3DXSaveUserData:: саветемплатес**](id3dxsaveuserdata--savetemplates.md) предоставляют механизм для добавления шаблона в файл. x для сохранения пользовательских данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
