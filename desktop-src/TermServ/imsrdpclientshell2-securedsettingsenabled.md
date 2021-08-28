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
ms.openlocfilehash: d418df76de38313d681f9f01a4dea33ba0803ad67e42d92d90d2ba5a354a8eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870884"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

 





