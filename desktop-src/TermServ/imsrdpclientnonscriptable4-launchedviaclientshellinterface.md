---
title: IMsRdpClientNonScriptable4 Лаунчедвиаклиентшеллинтерфаце, свойство
description: Указывает, запустил ли пользователь клиентский элемент управления с помощью интерфейса удаленный рабочий стол Веб-доступ (RD Веб-доступ).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Лаунчедвиаклиентшеллинтерфаце
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988859"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>Свойство IMsRdpClientNonScriptable4:: Лаунчедвиаклиентшеллинтерфаце

Указывает, запустил ли пользователь клиентский элемент управления с помощью интерфейса удаленный рабочий стол Веб-доступ (RD Веб-доступ).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a>Значение свойства

Задает свойство **лаунчедвиаклиентшеллинтерфаце** .

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

 

 





