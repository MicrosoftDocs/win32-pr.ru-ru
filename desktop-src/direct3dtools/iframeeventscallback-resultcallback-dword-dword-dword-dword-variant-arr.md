---
description: Функция обратного вызова, используемая для уведомления узла о событиях в списке событий.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентскаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1b6cf33869fce9dc51df8dcd58f98b0cc17a5f44
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623970"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Метод Ифрамивентскаллбакк:: Ресулткаллбакк

Функция обратного вызова, используемая для уведомления узла о событиях в списке событий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a>Параметры

*фраменумбер*   
Номер кадра, связанный с событиями.

*нумелементс*   
Общее число полей во всех столбцах всех событий.

*нумровс*   
Число событий в результате.

*нумколумнс*   
Число столбцов (полей) в каждой строке.

*count1 \_ провдата*   
Сведения о событиях; один элемент для каждого поля каждого события.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ифрамивентскаллбакк**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
