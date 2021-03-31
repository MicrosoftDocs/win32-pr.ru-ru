---
description: Функция обратного вызова, используемая для уведомления узла о данных таблицы объектов.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблекаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806695"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>Метод Иобжекттаблекаллбакк:: Ресулткаллбакк

Функция обратного вызова, используемая для уведомления узла о данных таблицы объектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a>Параметры

*нумелементс*   
Общее число полей во всех столбцах всех объектов.

*нумровс*   
Число передаваемых объектов.

*нумколумнс*   
Количество столбцов (полей) данных, передаваемых для каждого объекта.

*count0 \_ провдата*   
Сведения об объектах; по одному элементу для каждого поля каждого объекта.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иобжекттаблекаллбакк**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
