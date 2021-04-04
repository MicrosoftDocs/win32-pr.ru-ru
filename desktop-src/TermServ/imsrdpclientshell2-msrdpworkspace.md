---
title: IMsRdpClientShell2 Мсрдпворкспаце, свойство
description: Получает указатель на интерфейс Имсрдпворкспаце, используемый для управления учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Мсрдпворкспаце
- Службы удаленных рабочих столов свойства Мсрдпворкспаце, интерфейс IMsRdpClientShell2
- Службы удаленных рабочих столов интерфейса IMsRdpClientShell2, свойство Мсрдпворкспаце
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802950"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>Свойство IMsRdpClientShell2:: Мсрдпворкспаце

Получает указатель на интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) , используемый для управления учетными данными и соединениями подключения к удаленным рабочим столам и приложениям RemoteApp.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Значение свойства

Адрес указателя на интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) .

## <a name="remarks"></a>Комментарии

Интерфейс [**имсрдпворкспаце**](imsrdpworkspace.md) не предоставляется как пользовательский интерфейс. Доступ к нему возможен только через методы [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

