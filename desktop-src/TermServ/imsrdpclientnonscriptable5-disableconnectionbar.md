---
title: IMsRdpClientNonScriptable5 Дисаблеконнектионбар, свойство
description: указывает, должен ли элемент управления ActiveX удаленный рабочий стол отключить панель подключения.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисаблеконнектионбар
- Службы удаленных рабочих столов свойства Дисаблеконнектионбар, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Дисаблеконнектионбар
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f74fce650eb82514538eed7066b937c29f8618aba1eab7531f3bdb7e1127da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138747"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a>IMsRdpClientNonScriptable5: свойство Исаблеконнектионбар:D

указывает, должен ли элемент управления ActiveX удаленный рабочий стол отключить панель подключения. Если это свойство содержит **вариант \_ true**, панель подключения должна быть отключена. Если это свойство содержит **\_ значение Variant false**, то панель подключения должна быть включена.

Это свойство доступно только на запись.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a>Значение свойства

Указывает новое значение свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





