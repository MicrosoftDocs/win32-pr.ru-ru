---
description: Нарисуйте несколько экземпляров одного подмножества сетки.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: 'ID3DX10Mesh: метод:D Равсубсетинстанцед (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674740"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh: метод:D Равсубсетинстанцед

Нарисуйте несколько экземпляров одного подмножества сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аттрибид* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Указывает подмножество рисуемой сетки. Это значение используется для различения лиц в сетке как принадлежащих одной или нескольким группам атрибутов. См. примечания.

</dd> <dt>

*InstanceCount* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число экземпляров для подготовки к просмотру.

</dd> <dt>

*Стартинстанцелокатион* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Экземпляр, с которого начинается выборка из каждого буфера, помеченного как данные экземпляра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Сетка содержит таблицу атрибутов. Таблица атрибутов может разделить сетку на подмножества, где каждое подмножество определяется с помощью идентификатора атрибута. Например, сетка с 200 лицами, разделенная на три подмножества, может иметь таблицу атрибутов, которая выглядит следующим образом:



|            |                 |
|------------|-----------------|
| Аттрибид 0 | Лица 0 ~ 50    |
| Аттрибид 1 | Лица 51 ~ 125  |
| Аттрибид 2 | Лица 126 ~ 200 |



 

Создание экземпляров может увеличить производительность, повторно используя ту же геометрию для рисования нескольких объектов в сцене. Одним из примеров создания экземпляров может быть Рисование одного и того же объекта с разными позициями и цветами. Для индексирования требуется несколько буферов вершин: по крайней мере один для данных на вершину и второй буфер для данных каждого экземпляра.

Отрисовка экземпляров с помощью Дравсубсетинстанцед очень похожа на процесс, используемый с [**ID3D10Device::D равиндексединстанцед**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) , который описан в [примере](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)с созданием экземпляров. Ключевое различие при использовании Дравсубсетинстанцед заключается в том, что буферы вершин и индексы должны быть извлечены из объекта [**интерфейса ID3DX10Mesh**](id3dx10mesh.md) , прежде чем можно будет объединить данные о создании экземпляров.

Следующий код иллюстрирует извлечение буферов вершин и индексов из объекта сетки.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
