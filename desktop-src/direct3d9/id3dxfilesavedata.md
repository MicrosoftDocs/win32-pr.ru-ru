---
description: Приложения используют методы интерфейса ID3DXFileSaveData для добавления объектов данных в качестве дочерних элементов узла данных файла. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Интерфейс ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68d52c1c022ed292a879ae4f701df52524d4170160bc79b6f1956c744a530c22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121306"
---
# <a name="id3dxfilesavedata-interface"></a>Интерфейс ID3DXFileSaveData

Приложения используют методы интерфейса ID3DXFileSaveData для добавления объектов данных в качестве дочерних элементов узла данных файла. x.

## <a name="members"></a>Элементы

Интерфейс **ID3DXFileSaveData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveData** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXFileSaveData** содержит следующие методы.



| Метод                                                          | Описание                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**адддатаобжект**](id3dxfilesavedata--adddataobject.md)       | Добавляет объект данных в качестве дочернего элемента для узла данных файла **ID3DXFileSaveData** .<br/>                                                      |
| [**адддатареференце**](id3dxfilesavedata--adddatareference.md) | Добавляет ссылку на данные в качестве дочернего элемента для этого узла данных **ID3DXFileSaveData** File. Ссылка на данные указывает на объект данных файла.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Извлекает идентификатор GUID для этого узла данных файла **ID3DXFileSaveData** .<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Извлекает имя этого узла данных файла **ID3DXFileSaveData** .<br/>                                                                |
| [**Сохранение**](id3dxfilesavedata--getsave.md)                   | Получает указатель на этот узел данных файла [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Получает идентификатор шаблона для этого узла файловых данных.<br/>                                                                               |



 

## <a name="remarks"></a>Remarks

Идентификатор GUID для интерфейса ID3DXFileSaveObject — IID \_ ID3DXFileSaveObject.

Тип LPD3DXFileSaveData определяется как указатель на этот интерфейс.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файловые интерфейсы D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
