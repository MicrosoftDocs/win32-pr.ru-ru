---
description: Приложения используют методы интерфейса ID3DXFileEnumObject для прохода по объектам данных дочерних файлов в файле и для получения дочернего объекта по его глобальному уникальному идентификатору (GUID) или по имени.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Интерфейс ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c274a42a5e07f05af3b0b2ffe18dc3fbaf546591f23e6f24906cd1723578303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121363"
---
# <a name="id3dxfileenumobject-interface"></a>Интерфейс ID3DXFileEnumObject

Приложения используют методы интерфейса ID3DXFileEnumObject для прохода по объектам данных дочерних файлов в файле и для получения дочернего объекта по его глобальному уникальному идентификатору (GUID) или по имени.

## <a name="members"></a>Элементы

Интерфейс **ID3DXFileEnumObject** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileEnumObject** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXFileEnumObject** содержит следующие методы.



| Метод                                                                  | Описание                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Извлекает дочерний объект в этом объекте данных файла.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Возвращает количество дочерних объектов в этом объекте данных файла.<br/> |
| [**жетдатаобжектбид**](id3dxfileenumobject--getdataobjectbyid.md)     | Извлекает объект данных с указанным GUID.<br/>          |
| [**жетдатаобжектбинаме**](id3dxfileenumobject--getdataobjectbyname.md) | Извлекает объект данных с указанным именем.<br/>          |
| [**Файл.**](id3dxfileenumobject--getfile.md)                         | Извлекает объект [**ID3DXFile**](id3dxfile.md) .<br/>            |



 

## <a name="remarks"></a>Remarks

Идентификатор GUID для интерфейса ID3DXFileEnumObject — IID \_ ID3DXFileEnumObject.

Тип LPD3DXFILEENUMOBJECT определяется как указатель на этот интерфейс.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
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

 

 
