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
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423142"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ибуфферобжектдатакаллбакк**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
