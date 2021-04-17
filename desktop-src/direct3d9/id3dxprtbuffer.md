---
description: Интерфейс ID3DXPRTBuffer используется в качестве буфера данных для хранения данных вершин и точек для использования с предварительно вычисленными методами и функциями пересчета радианце (PRT).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Интерфейс ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704021"
---
# <a name="id3dxprtbuffer-interface"></a>Интерфейс ID3DXPRTBuffer

Интерфейс ID3DXPRTBuffer используется в качестве буфера данных для хранения данных вершин и точек для использования с предварительно вычисленными методами и функциями пересчета радианце (PRT).

## <a name="members"></a>Элементы

Интерфейс **ID3DXPRTBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTBuffer** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXPRTBuffer** содержит следующие методы.



| Метод                                                   | Описание                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддбуффер**](id3dxprtbuffer--addbuffer.md)           | Добавляет еще один буфер в **ID3DXPRTBuffer** и сохраняет результаты в **ID3DXPRTBuffer**.<br/>                                                                                        |
| [**аттачгх**](id3dxprtbuffer--attachgh.md)             | Связывает объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом **ID3DXPRTBuffer** .<br/>                                                              |
| [**евалгх**](id3dxprtbuffer--evalgh.md)                 | Применяет сохраненные данные для переплета текстуры в буфер текстуры **ID3DXPRTBuffer** .<br/>                                                                                                        |
| [**екстракттекстуре**](id3dxprtbuffer--extracttexture.md) | Извлекает данные коэффициента из цветового канала буфера для указанного диапазона коэффициентов и добавляет данные в объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**екстракттомеш**](id3dxprtbuffer--extracttomesh.md)   | Извлекает коэффициенты из одноканального буфера и добавляет данные в объект [**ID3DXMesh**](id3dxmesh.md) .<br/>                                                              |
| [**Высота**](id3dxprtbuffer--getheight.md)           | Получает высоту текстуры в пикселях.<br/>                                                                                                                                    |
| [**жетнумчаннелс**](id3dxprtbuffer--getnumchannels.md) | Возвращает количество цветовых каналов, используемых в памяти для хранения образцов.<br/>                                                                                                            |
| [**жетнумкоеффс**](id3dxprtbuffer--getnumcoeffs.md)     | Возвращает число скаляров на цветовой канал, используемый в памяти для хранения выборок.<br/>                                                                                                 |
| [**жетнумсамплес**](id3dxprtbuffer--getnumsamples.md)   | Возвращает число вершин (или пикселей текстуры) выборки.<br/>                                                                                                                              |
| [**Полуширинные**](id3dxprtbuffer--getwidth.md)             | Получает ширину текстуры в пикселях.<br/>                                                                                                                                     |
| [**«Текстурирование»**](id3dxprtbuffer--istexture.md)           | Указывает, содержит ли буфер текстуру.<br/>                                                                                                                                   |
| [**локкбуффер**](id3dxprtbuffer--lockbuffer.md)         | Блокирует диапазон демонстрационных данных вершин или шаг текселя и получает указатель на расположение в буферной памяти.<br/>                                                                               |
| [**релеасегх**](id3dxprtbuffer--releasegh.md)           | Отменяет связь присоединенного объекта [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом **ID3DXPRTBuffer** .<br/>                                                   |
| [**Изменить размер**](id3dxprtbuffer--resize.md)                 | Изменяет число выборок, содержащихся в буфере.<br/>                                                                                                                             |
| [**скалебуффер**](id3dxprtbuffer--scalebuffer.md)       | Умножает каждое значение в буфере на постоянное значение.<br/>                                                                                                                          |
| [**унлоккбуффер**](id3dxprtbuffer--unlockbuffer.md)     | Завершает срок существования указателя Ппдата, возвращенного [**ID3DXPRTBuffer:: локкбуффер**](id3dxprtbuffer--lockbuffer.md).<br/>                                                              |



 

## <a name="remarks"></a>Комментарии

Интерфейс **ID3DXPRTBuffer** получается путем вызова функций [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) или [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .

Тип LPD3DXPRTBUFFER определяется как указатель на интерфейс **ID3DXPRTBuffer** .


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
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

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
