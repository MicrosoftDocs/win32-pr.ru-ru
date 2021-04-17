---
title: IMsRdpClientShell2 Секуредсеттингсенаблед, свойство
description: Получает значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClientShell2
- Службы удаленных рабочих столов интерфейса IMsRdpClientShell2, свойство Секуредсеттингсенаблед
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672836"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>Свойство IMsRdpClientShell2:: Секуредсеттингсенаблед

Получает значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Значение свойства

Указатель на логическое значение, указывающее, находится ли текущая веб-страница в доверенной зоне безопасности URL-адреса Internet Explorer.

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

 

 





