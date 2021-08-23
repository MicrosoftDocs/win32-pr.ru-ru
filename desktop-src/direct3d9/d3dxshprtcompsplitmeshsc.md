---
description: Функция D3DXSHPRTCompSplitMeshSC — используется со сжатыми результатами эмулятора предварительно вычисленной радианценой пересылки (PRT).
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Функция D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14b138ae4c1b61b70147726d1a320e8dca1c0a57ffb11dd742419a46f9d131b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630874"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>Функция D3DXSHPRTCompSplitMeshSC

Используется с сжатыми результатами симулятора предварительно вычисленной радианценой пересылки (PRT). После вызова [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) эту функцию можно использовать для разделения сетки на группу лиц или вершин на супер-кластер. Каждый супер кластер содержит все грани, которые содержат любую вершину, классифицированную в одном из его кластеров. Все вершины, подключенные к этому набору лиц, также включаются в возвращаемый массив Ппвертстатус, который указывает, принадлежит ли вершина к Super кластеру.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклустеридс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Идентификаторы кластера *нумвертицес* (извлеченные из сжатого буфера).

</dd> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество вершин в исходной сетке.

</dd> <dt>

*Нумкс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество кластеров (входной параметр для сжатия).

</dd> <dt>

*псклустеридс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Массив размера *нумкс* , который будет содержать идентификаторы Super Cluster.

</dd> <dt>

*Нумскс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество супер кластеров, выделенных в [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*пинпутиб* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Буфер необработанных индексов для сетки. Формат зависит от *InputIBIs32Bit*.

</dd> <dt>

*InputIBIs32Bit* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение — true**, буфер индекса имеет значение 32 бит; в противном случае — 16 бит.

</dd> <dt>

*Нумфацес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число граней в исходной сети (*пинпутиб* в три раза больше этой длины).

</dd> <dt>

*ппибдата* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер необработанных индексов, который будет содержать полученные разделенные фрагменты. Формат, определенный параметром *InputIBIs32Bit*. Выделено функцией.

</dd> <dt>

*пибдаталенгс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Длина *ппибдата*, назначенная в функции.

</dd> <dt>

*OutputIBIs32Bit* \[ в, out\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение — true**, выделяет массив целых чисел без знака; в противном случае выделяет короткий массив без знака.

</dd> <dt>

*ппфацеремап* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Сопоставление каждого лица в *ппибдата* с исходными лицами. Длина — \* *пибдаталенгс*/3.

</dd> <dt>

*ппвертдата* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Новая структура данных вершин. Размер *пвертдаталенгс*.

</dd> <dt>

*пвертдаталенгс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Количество новых вершин в разделенной сетке. Назначено в функции.

</dd> <dt>

*пскклустерлист* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Массив длины, *нумкс* , что *пскдата* индексы в (поля *пклустеридс* \* ) для каждого кластера, содержит кластеры, упорядоченные по подкластерам.

</dd> <dt>

*пскдата* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Структура на супер кластер. Содержит индексы в *ппибдата*, *пскклустерлист* и *ппвертдата*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
