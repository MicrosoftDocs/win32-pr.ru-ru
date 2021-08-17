---
description: Интерфейс ID3DXSprite предоставляет набор методов, упрощающих процесс рисования спрайтов с помощью Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Интерфейс ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d5786096fb9c38188d73d613fd11efd97c2401e9f8ae9c7eb4a05dfe1dc1e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729250"
---
# <a name="id3dxsprite-interface"></a>Интерфейс ID3DXSprite

Интерфейс ID3DXSprite предоставляет набор методов, упрощающих процесс рисования спрайтов с помощью Microsoft Direct3D.

## <a name="members"></a>Элементы

Интерфейс **ID3DXSprite** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSprite** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXSprite** содержит следующие методы.



| Метод                                                | Описание                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Начать**](id3dxsprite--begin.md)                   | Подготавливает устройство для рисования спрайтов.<br/>                                                                                                                                                                            |
| [**Draw**](id3dxsprite--draw.md)                     | Добавляет спрайт в список пакетных спрайтов.<br/>                                                                                                                                                                     |
| [**Конец**](id3dxsprite--end.md)                       | Вызывает [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) и восстанавливает состояние устройства до вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .<br/>                                            |
| [**Очистка**](id3dxsprite--flush.md)                   | Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md). Затем список пакетных спрайтов удаляется.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Извлекает устройство, связанное с объектом Sprite.<br/>                                                                                                                                                           |
| [**Преобразование**](id3dxsprite--gettransform.md)     | Возвращает преобразование спрайта.<br/>                                                                                                                                                                                        |
| [**онлостдевице**](id3dxsprite--onlostdevice.md)     | Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.<br/>                              |
| [**онресетдевице**](id3dxsprite--onresetdevice.md)   | Этот метод используется для повторного получения ресурсов и сохранения начального состояния.<br/>                                                                                                                                                   |
| [**сеттрансформ**](id3dxsprite--settransform.md)     | Задает преобразование спрайта.<br/>                                                                                                                                                                                        |
| [**сетворлдвиевлх**](id3dxsprite--setworldviewlh.md) | Задает для спрайта левое преобразование представления мира. Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.<br/>                                                                                 |
| [**сетворлдвиеврх**](id3dxsprite--setworldviewrh.md) | Задает для спрайта правое преобразование представления мира. Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.<br/>                                                                                |



 

## <a name="remarks"></a>Remarks

Интерфейс **ID3DXSprite** получается путем вызова функции [**D3DXCreateSprite**](d3dxcreatesprite.md) .

Приложение, как правило, сначала вызывает [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), что позволяет управлять состоянием отрисовки устройства, альфа-смешением и преобразованием и сортировкой спрайтов. Затем для отображения каждого спрайта вызовите [**ID3DXSprite::D RAW**](id3dxsprite--draw.md). **ID3DXSprite::D RAW** можно вызывать многократно для хранения любого числа спрайтов. Чтобы отобразить пакетные спрайты на устройстве, вызовите метод [**ID3DXSprite:: end**](id3dxsprite--end.md) или [**ID3DXSprite:: Flush**](id3dxsprite--flush.md).

Тип LPD3DXSPRITE определяется как указатель на интерфейс **ID3DXSprite** .


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
