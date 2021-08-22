---
title: IMsRdpClientNonScriptable5 Алловпромптингфоркредентиалс, свойство
description: указывает, может ли элемент управления ActiveX удаленный рабочий стол запрашивать учетные данные у пользователя.
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
ms.openlocfilehash: eea0fb854b5bb12533032cd6608228d81584cd8d9f4e99bccd8a5ba76b624f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138757"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>Свойство IMsRdpClientNonScriptable5:: Алловпромптингфоркредентиалс

указывает, может ли элемент управления ActiveX удаленный рабочий стол запрашивать учетные данные у пользователя. Если это свойство содержит **вариант \_ true**, пользователю может быть предложено ввести учетные данные. Если это свойство содержит **вариант \_ false**, пользователю не может быть предложено ввести учетные данные.

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

 

 





