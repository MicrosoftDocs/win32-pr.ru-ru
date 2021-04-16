---
description: Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Интерфейс ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664969"
---
# <a name="id3dxsaveuserdata-interface"></a>Интерфейс ID3DXSaveUserData

Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x. Экземпляр этого интерфейса передается в [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), и D3DX вызывает соответствующий метод для этого интерфейса каждый раз при обнаружении соответствующих данных. Например, для каждого объекта Frame в файле. x вызывается [**ID3DXSaveUserData:: аддфрамечилддата**](id3dxsaveuserdata--addframechilddata.md) и ему передаются дочерние данные.

## <a name="members"></a>Элементы

Интерфейс **ID3DXSaveUserData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSaveUserData** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXSaveUserData** содержит следующие методы.



| Метод                                                                              | Описание                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**аддфрамечилддата**](id3dxsaveuserdata--addframechilddata.md)                   | Добавьте дочерние данные в рамку.<br/>                            |
| [**аддмешчилддата**](id3dxsaveuserdata--addmeshchilddata.md)                     | Добавление дочерних данных в сетку.<br/>                             |
| [**аддтоплевелдатаобжектспост**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Добавьте объект верхнего уровня после иерархии Frame.<br/>       |
| [**аддтоплевелдатаобжектспре**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Добавьте объект верхнего уровня перед иерархией Frame.<br/>      |
| [**регистертемплатес**](id3dxsaveuserdata--registertemplates.md)                   | Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.<br/> |
| [**саветемплатес**](id3dxsaveuserdata--savetemplates.md)                           | Обратный вызов для пользователя при сохранении шаблона файла. x.<br/>     |



 

## <a name="remarks"></a>Комментарии

Тип LPD3DXSAVEUSERDATA определяется как указатель на этот интерфейс.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
