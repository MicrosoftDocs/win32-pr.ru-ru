---
description: Обратный вызов, уведомляющий узел о том, что сведения о буфере записаны в файл с помощью запроса связана.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ибуфферобжектдатакаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eaf084402c1cc34bff83d3b50002fbdcf3d97fb1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623100"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Метод Ибуфферобжектдатакаллбакк:: Ресулткаллбакк

Обратный вызов, уведомляющий узел о том, что сведения о буфере записаны в файл с помощью запроса связана.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a>Параметры

*Файл* Строка COM, содержащая путь к файлу, в который записываются результаты.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается с ошибкой, возвращается **S_OK**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ибуфферобжектдатакаллбакк**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
