---
description: Интерфейс ID3DXRenderToSurface используется для обобщения процесса отрисовки на поверхности.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Интерфейс ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355823"
---
# <a name="id3dxrendertosurface-interface"></a>Интерфейс ID3DXRenderToSurface

Интерфейс ID3DXRenderToSurface используется для обобщения процесса отрисовки на поверхности.

## <a name="members"></a>Элементы

Интерфейс **ID3DXRenderToSurface** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToSurface** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXRenderToSurface** содержит следующие методы.



| Метод                                                       | Описание                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**бегинсцене**](id3dxrendertosurface--beginscene.md)       | Начинает сцену.<br/>                                                                                                                                                                      |
| [**ендсцене**](id3dxrendertosurface--endscene.md)           | Завершает сцену.<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | Извлекает параметры поверхности рендеринга.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Извлекает устройство Direct3D, связанное с областью прорисовки.<br/>                                                                                                                    |
| [**онлостдевице**](id3dxrendertosurface--onlostdevice.md)   | Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.<br/> |
| [**онресетдевице**](id3dxrendertosurface--onresetdevice.md) | Этот метод используется для повторного получения ресурсов и сохранения начального состояния.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Комментарии

Поверхности могут использоваться различными способами, включая цели рендеринга, отрисовку на экране или отрисовку текстур.

Поверхность можно настроить с помощью отдельного окна просмотра с помощью метода [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md) , чтобы предоставить пользовательское представление отрисовки. Если поверхность не является целевым объектом отрисовки, используется совместимый целевой объект рендеринга, и результат копируется в область в конце сцены.

Интерфейс **ID3DXRenderToSurface** получается путем вызова функции [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .

Тип LPD3DXRENDERTOSURFACE определяется как указатель на интерфейс **ID3DXRenderToSurface** .


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
