---
description: Обратный вызов, уведомляющий узел о том, что данные сетки этапа конвейера возвращены запросом связана.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Мешдатаверткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c91cb5faedf183fbf6afcbf462a10ce928a1024745ae4973c5aac08063d05f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484892"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Метод Ипипелинестажескаллбакк:: Мешдатаверткаллбакк

Обратный вызов, уведомляющий узел о том, что данные сетки этапа конвейера возвращены запросом связана.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>Параметры

*нумвертицес*   
Число вершин в результатах.

*нумбуфферлайаутентриес*   
Число записей макета буфера в результатах.

*\_записи count1*   
Макет буфера целиком. Они описывают выходную подпись шейдера.

*шага*   
Размер (STRIDE) всего выходного блока.

*нумвббитес*   
Размер буфера вершин в байтах.

*count4 \_ пвбдата*   
Буфер вершин.

*нумиббитес*   
Размер буфера индекса в байтах.

*count6 \_ пибдата*   
Буфер индекса.

*indexSize*   
Размер каждого индекса в байтах.

*ибоффсет*   
Смещение в буфере индекса, указывающее, где должны начинаться индексы.

*басевертекс*   
Смещение в буфере вершин, которое указывает, где следует начинать использовать вершины.

*минвертекс*   

*ибиндексесвб*   
значение true, если используется буфер индекса; в противном случае — false.

*нуминдицес*   
Количество используемых индексов.

*Topology*   
Тополологи шейдера. Это не обязательно то же самое, что и топология связанного вызова Draw.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипипелинестажескаллбакк**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
