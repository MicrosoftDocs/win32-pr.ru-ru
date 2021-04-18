---
description: Интерфейс ID3DXPRTCompBuffer хранит сжатую версию буфера ID3DXPRTBuffer для использования с анализом основных компонентов (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Интерфейс ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703972"
---
# <a name="id3dxprtcompbuffer-interface"></a>Интерфейс ID3DXPRTCompBuffer

Интерфейс **ID3DXPRTCompBuffer** хранит сжатую версию буфера [**ID3DXPRTBuffer**](id3dxprtbuffer.md) для использования с анализом основных компонентов (PCA).

## <a name="members"></a>Элементы

Интерфейс **ID3DXPRTCompBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTCompBuffer** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXPRTCompBuffer** содержит следующие методы.



| Метод                                                             | Описание                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**екстрактбасис**](id3dxprtcompbuffer--extractbasis.md)           | Извлекает средние и абстрактные векторы для заданного кластера из сжатого буфера данных **ID3DXPRTCompBuffer** .<br/>                                                                       |
| [**екстрактклустеридс**](id3dxprtcompbuffer--extractclusterids.md) | Извлекает идентификаторы кластеров по образцу из сжатого буфера данных **ID3DXPRTCompBuffer** .<br/>                                                                                                                              |
| [**екстрактпка**](id3dxprtcompbuffer--extractpca.md)               | Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных **ID3DXPRTCompBuffer** .<br/>                                                                               |
| [**екстракттекстуре**](id3dxprtcompbuffer--extracttexture.md)       | Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных **ID3DXPRTCompBuffer** и добавляет их в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**екстракттомеш**](id3dxprtcompbuffer--extracttomesh.md)         | Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных **ID3DXPRTCompBuffer** и добавляет их в объект [**ID3DXMesh**](id3dxmesh.md) .<br/>                 |
| [**Высота**](id3dxprtcompbuffer--getheight.md)                 | Получает высоту текстуры в пикселях.<br/>                                                                                                                                                                         |
| [**жетнумчаннелс**](id3dxprtcompbuffer--getnumchannels.md)       | Возвращает количество цветовых каналов, используемых в памяти для хранения образцов.<br/>                                                                                                                                                 |
| [**жетнумклустерс**](id3dxprtcompbuffer--getnumclusters.md)       | Извлекает количество кластеров, используемых для сжатия.<br/>                                                                                                                                                                |
| [**жетнумкоеффс**](id3dxprtcompbuffer--getnumcoeffs.md)           | Возвращает число скаляров на цветовой канал, используемый в памяти для хранения выборок.<br/>                                                                                                                                      |
| [**жетнумпка**](id3dxprtcompbuffer--getnumpca.md)                 | Извлекает количество основных векторов анализа компонентов (PCA) для использования в каждом кластере.<br/>                                                                                                                        |
| [**жетнумсамплес**](id3dxprtcompbuffer--getnumsamples.md)         | Возвращает число вершин (или пикселей текстуры) выборки.<br/>                                                                                                                                                                   |
| [**Полуширинные**](id3dxprtcompbuffer--getwidth.md)                   | Получает ширину текстуры в пикселях.<br/>                                                                                                                                                                          |
| [**«Текстурирование»**](id3dxprtcompbuffer--istexture.md)                 | Указывает, содержит ли буфер текстуру.<br/>                                                                                                                                                                        |
| [**нормализедата**](id3dxprtcompbuffer--normalizedata.md)         | Нормализует все весовые коэффициенты для анализа основных компонентов (PCA), чтобы они были в диапазоне от-1 до 1. Векторы базиса изменяются для отражения этой нормализации.<br/>                                                                  |



 

## <a name="remarks"></a>Комментарии

Интерфейс **ID3DXPRTCompBuffer** получается путем вызова функции [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .

Тип LPD3DXPRTCOMPBUFFER определяется как указатель на интерфейс **ID3DXPRTCompBuffer** .


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
