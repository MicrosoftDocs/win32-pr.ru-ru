---
description: ID3DX10SkinInfo позволяет оптимизировать, обрабатывать и вручную устанавливать связи между костями и вершинами в ваших сетках (см. статью анимация скелетообразных в Википедии).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Интерфейс ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354930"
---
# <a name="id3dx10skininfo-interface"></a>Интерфейс ID3DX10SkinInfo

ID3DX10SkinInfo позволяет оптимизировать, обрабатывать и вручную устанавливать связи между костями и вершинами в ваших сетках (см. статью [анимация скелетообразных в Википедии](https://en.wikipedia.org/wiki/Skeletal_animation)). Это наиболее полезно для создания файлов. x, экспортируемых приложениями ДКК (например, 3DS Max и Maya), более удобной для оборудования, а также для повышения скорости рендеринга в ролевых сетках в режиме рендеринга программного обеспечения.

## <a name="members"></a>Элементы

Интерфейс **ID3DX10SkinInfo** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10SkinInfo** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX10SkinInfo** содержит следующие методы.



| Метод                                                                   | Описание                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**аддбонеинфлуенцес**](id3dx10skininfo-addboneinfluences.md)           | Включите существующую кость, чтобы она влияла на группу вершин, и определите, насколько сильно влияют на эту кость на каждой вершине.<br/>     |
| [**аддбонес**](id3dx10skininfo-addbones.md)                             | Выделение пространства для дополнительных костей.<br/>                                                                                          |
| [**аддвертицес**](id3dx10skininfo-addvertices.md)                       | Выделение пространства для дополнительных вершин.<br/>                                                                                 |
| [**клеарбонеинфлуенцес**](id3dx10skininfo-clearboneinfluences.md)       | Очистите список вершин, которые она влияет на кость.<br/>                                                                     |
| [**Компактный**](id3dx10skininfo-compact.md)                               | Ограничьте число костей, которые могут повлиять на вершину и/или ограничить объем влияния на кость на вершину.<br/> |
| [**дософтварескиннинг**](id3dx10skininfo-dosoftwareskinning.md)         | Выпустить программное обеспечение на массиве вершин.<br/>                                                                           |
| [**финдбонеинфлуенцеиндекс**](id3dx10skininfo-findboneinfluenceindex.md) | Найдите индекс, указывающий, где заданная вершина находится в списке заданных вершин на заданной кости.<br/>                    |
| [**жетбонеинфлуенце**](id3dx10skininfo-getboneinfluence.md)             | Получение суммы влияния на заданную кость на заданную вершину.<br/>                                                       |
| [**жетбонеинфлуенцекаунт**](id3dx10skininfo-getboneinfluencecount.md)   | Возвращает количество вершин, на которые влияет заданная кость.<br/>                                                                |
| [**жетбонеинфлуенцес**](id3dx10skininfo-getboneinfluences.md)           | Получение списка вершин, на которые влияет заданная кость, и списка интенсивности влияния этой кости на каждую вершину.<br/> |
| [**жетмаксбонеинфлуенцес**](id3dx10skininfo-getmaxboneinfluences.md)     | Получите число вершин, которые могут максимально повлиять на кость.<br/>                                                              |
| [**жетнумбонес**](id3dx10skininfo-getnumbones.md)                       | Возвращает число костей в ID3DX10SkinInfo.<br/>                                                                             |
| [**жетнумвертицес**](id3dx10skininfo-getnumvertices.md)                 | Возвращает количество вершин в ID3DX10SkinInfo.<br/>                                                                          |
| [**ремапбонес**](id3dx10skininfo-remapbones.md)                         | Изменение того, какие кости влияют на вершины.<br/>                                                                            |
| [**ремапвертицес**](id3dx10skininfo-remapvertices.md)                   | Изменение вершин, на которые влияют эти кости.<br/>                                                                    |
| [**ремовебоне**](id3dx10skininfo-removebone.md)                         | Удалить кость.<br/>                                                                                                          |
| [**сетбонеинфлуенце**](id3dx10skininfo-setboneinfluence.md)             | Установка объема влияния на заданную кость на заданную вершину.<br/>                                                       |



 

## <a name="remarks"></a>Комментарии

Создание интерфейса ID3DX10SkinInfo с помощью [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** или **D3DX10CreateSkinInfoFVF**.

Тип LPD3DX10SKININFO определяется как указатель на интерфейс **ID3DX10SkinInfo** .


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
