---
description: Обратный вызов, уведомляющий основное приложение об универсальных буферах, возвращаемых запросом связана.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иженерикбуффердатакаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806514"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Метод Иженерикбуффердатакаллбакк:: Ресулткаллбакк

Обратный вызов, уведомляющий основное приложение об универсальных буферах, возвращаемых запросом связана.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a>Параметры

*изменять*   
Размер содержимого буфера в байтах.

*\_буфер count0*   
Содержимое буфера. В большинстве случаев это XML-данные.

*type*   
Строка COM, указывающая тип содержимого, возвращаемого в буфере.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иженерикбуффердатакаллбакк**](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
