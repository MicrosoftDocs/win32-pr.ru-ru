---
description: Запросы, указывающие, что в журнале графики есть новые данные.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine2:: Онневдатааваилабле'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bdfa8bdeb0140e9d8366deabc97b164dff8d4991
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628210"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>Метод IPixEngine2:: Онневдатааваилабле

Запросы, указывающие, что в журнале графики есть новые данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a>Параметры

*фсессионенд*   
значение true, если сеанс завершен; в противном случае — значение false.

*фунлоадкурфраме*   
Не используется.

*i64FilePositionStart*   
Расположение файла в байтах, с которого начинаются новые данные.

*i64FilePositionEnd*   
Расположение файла в байтах, в течение которого завершается новая операция.

*иобжекттабледатасизе*   
Число байтов, содержащихся в count4 \_ побжекттабледата.

*count4 \_ побжекттабледата*   
Буфер, содержащий данные для таблицы объектов.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
