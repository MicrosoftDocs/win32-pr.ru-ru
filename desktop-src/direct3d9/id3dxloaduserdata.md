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
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093632"
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
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
