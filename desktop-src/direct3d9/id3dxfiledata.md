---
description: Приложения используют методы интерфейса ID3DXFileData для создания или доступа к немедленной иерархии объекта данных. Иерархия определяется ограничениями шаблонов.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Интерфейс ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e85e66d5089183b1797842ab4e152a10298ebcc74a10c66291c6f6bc62743e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121430"
---
# <a name="id3dxfiledata-interface"></a>Интерфейс ID3DXFileData

Приложения используют методы интерфейса ID3DXFileData для создания или доступа к немедленной иерархии объекта данных. Иерархия определяется ограничениями шаблонов.

## <a name="members"></a>Элементы

Интерфейс **ID3DXFileData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileData** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXFileData** содержит следующие методы.



| Метод                                            | Описание                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetChild**](id3dxfiledata--getchild.md)       | Извлекает дочерний объект в этом объекте данных файла.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Возвращает количество дочерних элементов в этом объекте данных файла.<br/>                                                |
| [**Перечисление**](id3dxfiledata--getenum.md)         | Извлекает объект перечисления в этом объекте данных файла.<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | Извлекает идентификатор GUID для этого файлового объекта данных.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Извлекает имя этого файлового объекта данных.<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | Получает идентификатор шаблона в этом объекте данных файла.<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | Указывает, является ли данный файловый объект данных ссылочным объектом, указывающим на другой дочерний объект данных.<br/>   |
| [**Блокировка**](id3dxfiledata--lock.md)               | Обращается к данным файла. x.<br/>                                                                                |
| [**Блокирован**](id3dxfiledata--unlock.md)           | Завершает срок существования указателя *ппдата* , возвращенного [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).<br/> |



 

## <a name="remarks"></a>Remarks

Типы данных, разрешенные шаблоном, называются необязательными членами. Необязательные элементы не являются обязательными, но объект может пропустить важную информацию без них. Эти необязательные члены сохраняются как дочерние элементы объекта данных. Дочерний элемент может быть другим объектом данных или ссылкой на более раннюю версию объекта данных.

Идентификатор GUID для интерфейса ID3DXFileData — IID \_ ID3DXFileData.

Тип LPD3DXFILEDATA определяется как указатель на этот интерфейс.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 
