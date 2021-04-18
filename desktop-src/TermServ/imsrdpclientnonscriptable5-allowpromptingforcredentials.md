---
title: IMsRdpClientNonScriptable5 Алловпромптингфоркредентиалс, свойство
description: Указывает, может ли элемент управления удаленный рабочий стол ActiveX запрашивать учетные данные у пользователя.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Алловпромптингфоркредентиалс
- Службы удаленных рабочих столов свойства Алловпромптингфоркредентиалс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Алловпромптингфоркредентиалс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682146"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>Свойство IMsRdpClientNonScriptable5:: Алловпромптингфоркредентиалс

Указывает, может ли элемент управления удаленный рабочий стол ActiveX запрашивать учетные данные у пользователя. Если это свойство содержит **вариант \_ true**, пользователю может быть предложено ввести учетные данные. Если это свойство содержит **вариант \_ false**, пользователю не может быть предложено ввести учетные данные.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
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

 

 





