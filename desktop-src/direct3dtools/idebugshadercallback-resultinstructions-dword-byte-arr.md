---
description: Обратный вызов, уведомляющий узел о инструктрион данных, возвращаемых связанным запросом.
MS-HAID: vspixengine.IDebugShaderCallback\_ResultInstructions\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Идебугшадеркаллбакк:: Ресултинструктионс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 52440CE4-561C-4808-BE6A-B25A84BA5729
api_name:
- IDebugShaderCallback.ResultInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d8583d19d8da6225caee1135ae8553f71abfbe1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622950"
---
# <a name="span-idvspixengineidebugshadercallback_resultinstructions_dword_byte_arrspanidebugshadercallbackresultinstructions-method"></a><span id="vspixengine.idebugshadercallback_resultinstructions_dword_byte_arr"></span>Метод Идебугшадеркаллбакк:: Ресултинструктионс

Обратный вызов, уведомляющий узел о инструктрион данных, возвращаемых связанным запросом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultInstructions(
   DWORD   instructionStreamSize,
   BYTE [] count0_instructionStream
);
```

## <a name="parameters"></a>Параметры

*инструктионстреамсизе*   
Количество инструкций.

*count0 \_ инструктионстреам*   
Инструкции.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**идебугшадеркаллбакк**](/windows/desktop/direct3dtools/idebugshadercallback)

 

 
