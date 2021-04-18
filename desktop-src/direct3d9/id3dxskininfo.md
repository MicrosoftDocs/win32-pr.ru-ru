---
description: Приложения используют методы интерфейса ID3DXSkinInfo для управления матрицами костей, которые используются для обложки данных вершин для анимации. Этот интерфейс более строго привязан к ID3DXMesh и может использоваться для обложек любого набора данных вершин.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Интерфейс ID3DXSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713593"
---
# <a name="id3dxskininfo-interface"></a>Интерфейс ID3DXSkinInfo

Приложения используют методы интерфейса ID3DXSkinInfo для управления матрицами костей, которые используются для обложки данных вершин для анимации. Этот интерфейс более строго привязан к [**ID3DXMesh**](id3dxmesh.md) и может использоваться для обложек любого набора данных вершин.

## <a name="members"></a>Элементы

Интерфейс **ID3DXSkinInfo** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSkinInfo** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXSkinInfo** содержит следующие методы.



| Метод                                                                              | Описание                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Клонировать**](id3dxskininfo--clone.md)                                               | Создает точную копию объекта сведений об обложке.<br/>                                                                                                                                                          |
| [**конверттоблендедмеш**](id3dxskininfo--converttoblendedmesh.md)                 | Принимает сетку и возвращает новую сетку с весовым коэффициентом смешения и таблицей сочетаний костей. В таблице описывается, какие кости влияют на подмножества сетки.<br/>                   |
| [**конверттоиндекседблендедмеш**](id3dxskininfo--converttoindexedblendedmesh.md)   | Принимает сетку и возвращает новую сетку с весовыми коэффициентами перехода на вершину, индексами и комбинацией костей. В таблице описывается, какие палитры костей влияют на подмножества сетки.<br/> |
| [**финдбоневертексинфлуенцеиндекс**](id3dxskininfo--findbonevertexinfluenceindex.md) | Извлекает индекс кости, влияющей на одну вершину.<br/>                                                                                                                |
| [**жетбонеинфлуенце**](id3dxskininfo--getboneinfluence.md)                         | Возвращает вершины и весовые коэффициенты, влияющие на кость.<br/>                                                                                                                               |
| [**жетбоненаме**](id3dxskininfo--getbonename.md)                                   | Возвращает имя кости из индекса костей.<br/>                                                                                                                                            |
| [**жетбонеоффсетматрикс**](id3dxskininfo--getboneoffsetmatrix.md)                   | Возвращает матрицу смещения кости.<br/>                                                                                                                                                        |
| [**жетбоневертексинфлуенце**](id3dxskininfo--getbonevertexinfluence.md)             | Извлекает коэффициент смешения и вершину, затрагиваемые указанными костями.<br/>                                                                                                       |
| [**Объявление о выходе**](id3dxskininfo--getdeclaration.md)                             | Возвращает объявление вершины.<br/>                                                                                                                                                        |
| [**жетфвф**](id3dxskininfo--getfvf.md)                                             | Возвращает значение фиксированной вершины функции.<br/>                                                                                                                                               |
| [**жетмаксфацеинфлуенцес**](id3dxskininfo--getmaxfaceinfluences.md)                 | Возвращает максимальное влияние на грань в сетке треугольников с указанным буфером индекса.<br/>                                                                                                |
| [**жетмаксвертексинфлуенцес**](id3dxskininfo--getmaxvertexinfluences.md)             | Возвращает максимальное количество влияния на любую вершину в сетке.<br/>                                                                                                                   |
| [**жетминбонеинфлуенце**](id3dxskininfo--getminboneinfluence.md)                   | Возвращает минимальную влияние на кость. Влияние значений меньше этого значения не учитывается.<br/>                                                                                                    |
| [**жетнумбонеинфлуенцес**](id3dxskininfo--getnumboneinfluences.md)                 | Возвращает число повлияет на кость.<br/>                                                                                                                                           |
| [**жетнумбонес**](id3dxskininfo--getnumbones.md)                                   | Возвращает число костей.<br/>                                                                                                                                                           |
| [**Восстановить**](id3dxskininfo--remap.md)                                               | Обновляет сведения, влияющие на кости, для сопоставления вершин после их переупорядочивания. Этот метод должен вызываться, если целевой буфер вершин был изменен заказа извне.<br/>              |
| [**сетбонеинфлуенце**](id3dxskininfo--setboneinfluence.md)                         | Задает значение влияния для кости.<br/>                                                                                                                                                |
| [**сетбоненаме**](id3dxskininfo--setbonename.md)                                   | Задает имя кости.<br/>                                                                                                                                                                 |
| [**сетбонеоффсетматрикс**](id3dxskininfo--setboneoffsetmatrix.md)                   | Задает матрицу смещения кости.<br/>                                                                                                                                                        |
| [**сетбоневертексинфлуенце**](id3dxskininfo--setbonevertexinfluence.md)             | Задает значение влияния кости на одну вершину.<br/>                                                                                                                               |
| [**сетдекларатион**](id3dxskininfo--setdeclaration.md)                             | Задает объявление вершины.<br/>                                                                                                                                                        |
| [**сетфвф**](id3dxskininfo--setfvf.md)                                             | Задает тип гибкого формата вершин (ФВФ).<br/>                                                                                                                                         |
| [**сетминбонеинфлуенце**](id3dxskininfo--setminboneinfluence.md)                   | Устанавливает минимальную влияние на кость. Влияние значений меньше этого значения не учитывается.<br/>                                                                                                    |
| [**упдатескиннедмеш**](id3dxskininfo--updateskinnedmesh.md)                       | Применяет обложки программного обеспечения к целевым вершинам на основе текущих матриц.<br/>                                                                                                     |



 

## <a name="remarks"></a>Комментарии

Создание интерфейса **ID3DXSkinInfo** с помощью [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)или [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

Тип LPD3DXSKININFO определяется как указатель на интерфейс **ID3DXSkinInfo** .


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
