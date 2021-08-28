---
description: Возвращает сведения о том, какие столбцы (типы данных объектов) поддерживаются таблицей объектов.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблекаллбакк:: Жетсуппортедколумнс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c55c2e6f5ef304b031565148359bf96adeea248d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631382"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>Метод Иобжекттаблекаллбакк:: Жетсуппортедколумнс

Возвращает сведения о том, какие столбцы (типы данных объектов) поддерживаются таблицей объектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a>Параметры

*нумколумнс*   
Число столбцов, поддерживаемое таблицей объектов.

*count0_pIDs*   
Идентификаторы каждого столбца, поддерживаемого таблицей объектов.

*count0_pBstrNames*   
Имена каждого столбца в виде строки COM, поддерживаемой таблицей объектов.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается с ошибкой, возвращается **S_OK**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иобжекттаблекаллбакк**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
