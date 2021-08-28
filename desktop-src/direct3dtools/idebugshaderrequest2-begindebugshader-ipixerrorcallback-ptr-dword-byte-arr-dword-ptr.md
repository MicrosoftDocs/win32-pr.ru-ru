---
description: Запросы на запуск отладки указанного списка инструкций.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IDebugShaderRequest2:: Бегиндебугшадер'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3f59ef2da1fff99ca7ceee28a8c69554eb76047e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632102"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>Метод IDebugShaderRequest2:: Бегиндебугшадер

Запросы на запуск отладки указанного списка инструкций.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a>Параметры

*ерроркаллбакк*   
Адрес обратного вызова для ошибок, которые могут возникнуть во время отладки.

*инструктионстреамсизе*   
Количество инструкций в потоке инструкций.

*count1 \_ инструктионстреам*   
Указанный поток инструкций.

*пдевице*   
Адрес, который необходимо передать модулю отладки для взаимодействия с этим сеансом отладки (реадпроцессмемори отладчика по этому адресу).

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
