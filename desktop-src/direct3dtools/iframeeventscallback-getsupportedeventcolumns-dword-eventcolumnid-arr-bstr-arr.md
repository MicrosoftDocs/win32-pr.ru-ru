---
description: Возвращает сведения о том, какие столбцы (типы данных событий) поддерживаются списком событий.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентскаллбакк:: Жетсуппортедевентколумнс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b8f0443f47f3eca96388fd1df5ed91f8c05efe10
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630823"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>Метод Ифрамивентскаллбакк:: Жетсуппортедевентколумнс

Возвращает сведения о том, какие столбцы (типы данных событий) поддерживаются списком событий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a>Параметры

*нумколумнс*   
Число столбцов, поддерживаемое

*count0 \_ PID*   
Идентификаторы каждого столбца, поддерживаемого списком событий.

*count0 \_ пбстрнамес*   
Имена каждого столбца в виде строки COM, поддерживаемой списком событий.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ифрамивентскаллбакк**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
