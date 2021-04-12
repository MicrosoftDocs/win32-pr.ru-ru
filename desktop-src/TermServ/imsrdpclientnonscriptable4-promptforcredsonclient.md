---
title: IMsRdpClientNonScriptable4 Промптфоркредсонклиент, свойство
description: Указывает, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Промптфоркредсонклиент
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415769"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a>IMsRdpClientNonScriptable4: свойство Ромптфоркредсонклиент:P

Указывает, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a>Значение свойства

Определяет, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





