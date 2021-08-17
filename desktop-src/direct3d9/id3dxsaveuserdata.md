---
description: Интерфейс ID3DXSaveUserData. Этот интерфейс реализуется приложением для сохранения дополнительных пользовательских данных, внедренных в файлы. x.
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
ms.openlocfilehash: e5b0f02a4fb114f46930076f46ea7c416850a0e81f7369d4aab63a2de5ed6d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801140"
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



 

## <a name="remarks"></a>Remarks

Тип LPD3DXSAVEUSERDATA определяется как указатель на этот интерфейс.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
