---
description: Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Интерфейс ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713558"
---
# <a name="id3dxloaduserdata-interface"></a>Интерфейс ID3DXLoadUserData

Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x. Экземпляр этого интерфейса передается в [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), и D3DX вызывает соответствующий метод для этого интерфейса каждый раз при обнаружении соответствующих данных. Например, для каждого объекта Frame в файле. x вызывается [**ID3DXLoadUserData:: лоадфрамечилддата**](id3dxloaduserdata--loadframechilddata.md) и ему передаются дочерние данные.

## <a name="members"></a>Элементы

Интерфейс **ID3DXLoadUserData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLoadUserData** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXLoadUserData** содержит следующие методы.



| Метод                                                              | Описание                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**лоадфрамечилддата**](id3dxloaduserdata--loadframechilddata.md) | Загрузка дочерних данных фрейма из файла. x.<br/> |
| [**лоадмешчилддата**](id3dxloaduserdata--loadmeshchilddata.md)   | Загрузка дочерних данных сетки из файла. x.<br/>  |
| [**лоадтоплевелдата**](id3dxloaduserdata--loadtopleveldata.md)     | Загрузка данных верхнего уровня из файла. x.<br/>   |



 

## <a name="remarks"></a>Комментарии

Тип LPD3DXLOADUSERDATA определяется как указатель на этот интерфейс.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
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

 

 
