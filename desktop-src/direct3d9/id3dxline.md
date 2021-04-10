---
description: Интерфейс ID3DXLine реализует рисование линий с помощью текстурированных треугольников.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Интерфейс ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081954"
---
# <a name="id3dxline-interface"></a>Интерфейс ID3DXLine

Интерфейс ID3DXLine реализует рисование линий с помощью текстурированных треугольников.

## <a name="members"></a>Элементы

Интерфейс **ID3DXLine** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLine** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXLine** содержит следующие методы.



| Метод                                                | Описание                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Начать**](id3dxline--begin.md)                     | Подготавливает устройство для рисования линий.<br/>                                                                                                                                                  |
| [**Draw**](id3dxline--draw.md)                       | Рисует полосу линий в пространстве экрана. Входные данные указываются в виде массива, определяющего точки (of [**D3DXVECTOR2**](d3dxvector2.md)) на полосе строк.<br/>                                   |
| [**дравтрансформ**](id3dxline--drawtransform.md)     | Рисует полосу линий в пространстве экрана с заданной матрицей преобразования входных данных.<br/>                                                                                                      |
| [**END**](id3dxline--end.md)                         | Восстанавливает состояние устройства в том виде, в котором оно было при вызове [**ID3DXLine:: Begin**](id3dxline--begin.md) .<br/>                                                                                 |
| [**жетантиалиас**](id3dxline--getantialias.md)       | Возвращает состояние сглаживания линии.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Извлекает устройство Direct3D, связанное с объектом Line.<br/>                                                                                                                        |
| [**жетгллинес**](id3dxline--getgllines.md)           | Возвращает режим отображения линий в стиле OpenGL.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Возвращает шаблон линии стиппле.<br/>                                                                                                                                                        |
| [**жетпаттернскале**](id3dxline--getpatternscale.md) | Возвращает значение масштаба стиппле-pattern.<br/>                                                                                                                                                 |
| [**Полуширинные**](id3dxline--getwidth.md)               | Возвращает толщину линии.<br/>                                                                                                                                                       |
| [**онлостдевице**](id3dxline--onlostdevice.md)       | Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.<br/> |
| [**онресетдевице**](id3dxline--onresetdevice.md)     | Этот метод используется для повторного получения ресурсов и сохранения начального состояния.<br/>                                                                                                                       |
| [**сетантиалиас**](id3dxline--setantialias.md)       | Переключает Сглаживание линии.<br/>                                                                                                                                                            |
| [**сетгллинес**](id3dxline--setgllines.md)           | Переключает режим для отображения линий в стиле OpenGL.<br/>                                                                                                                                          |
| [**сетпаттерн**](id3dxline--setpattern.md)           | Применяет к строке шаблон стиппле.<br/>                                                                                                                                                |
| [**сетпаттернскале**](id3dxline--setpatternscale.md) | Растягивает шаблон стиппле вдоль направления линии.<br/>                                                                                                                               |
| [**сетвидс**](id3dxline--setwidth.md)               | Задает толщину линии.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Комментарии

Создайте объект рисования линий с помощью [**D3DXCreateLine**](d3dxcreateline.md).

Тип LPD3DXLINE определяется как указатель на интерфейс **ID3DXLine** .


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
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

 

 
