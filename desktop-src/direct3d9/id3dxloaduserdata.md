---
description: Интерфейс ID3DXLoadUserData. Этот интерфейс реализуется приложением для сохранения дополнительных пользовательских данных, внедренных в файлы. x.
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
ms.openlocfilehash: 9ede66e7250a1dec095bd03a72ea69e58afb59a60b43647fd49adfc958689cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748124"
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



 

## <a name="remarks"></a>Remarks

Тип LPD3DXLOADUSERDATA определяется как указатель на этот интерфейс.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
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

 

 
