---
description: Интерфейс ID3DXRenderToEnvMap используется для подготовки процесса визуализации к картам среды.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Интерфейс ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94fc32654ca5bea81538a5dc56e7ca6b391287703a4a96dfccf62ceae497766a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095774"
---
# <a name="id3dxrendertoenvmap-interface"></a>Интерфейс ID3DXRenderToEnvMap

Интерфейс ID3DXRenderToEnvMap используется для подготовки процесса визуализации к картам среды.

## <a name="members"></a>Элементы

Интерфейс **ID3DXRenderToEnvMap** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToEnvMap** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXRenderToEnvMap** содержит следующие методы.



| Метод                                                          | Описание                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**бегинкубе**](id3dxrendertoenvmap--begincube.md)             | Инициация отрисовки схемы кубической среды.<br/>                                                                                                                                    |
| [**бегинхемисфере**](id3dxrendertoenvmap--beginhemisphere.md) | Инициация отрисовки схемы среды хемисферик.<br/>                                                                                                                              |
| [**бегинпараболик**](id3dxrendertoenvmap--beginparabolic.md)   | Инициация отрисовки схемы среды параболическим.<br/>                                                                                                                                |
| [**бегинсфере**](id3dxrendertoenvmap--beginsphere.md)         | Инициация отрисовки сферической схемы среды.<br/>                                                                                                                                |
| [**Конец**](id3dxrendertoenvmap--end.md)                         | Восстановите все целевые объекты отрисовки и при необходимости сформируйте все отрисованные лица в области схемы среды.<br/>                                                                           |
| [**Распознавание лиц**](id3dxrendertoenvmap--face.md)                       | Инициирует рисование каждой грани схемы среды.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Извлекает описание поверхности рендеринга.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Извлекает устройство Direct3D, связанное с картой среды.<br/>                                                                                                                    |
| [**онлостдевице**](id3dxrendertoenvmap--onlostdevice.md)       | Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.<br/> |
| [**онресетдевице**](id3dxrendertoenvmap--onresetdevice.md)     | Этот метод используется для повторного получения ресурсов и сохранения начального состояния.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Remarks

Схема окружения используется для создания геометрии текстурной схемы, чтобы обеспечить более сложную сцену без использования сложной геометрии. Этот интерфейс поддерживает создание поверхностей для следующих видов геометрии: Cube, 1/2 Sphere или хемисферик, параболическим или Sphere.

Интерфейс **ID3DXRenderToEnvMap** получается путем вызова функции [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .

Тип LPD3DXRenderToEnvMap определяется как указатель на интерфейс **ID3DXRenderToEnvMap** .


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
