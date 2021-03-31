---
title: Иремотедесктопклиент Settings, свойство
description: Извлекает объект параметров для клиента контейнера приложения протокол удаленного рабочего стола (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Свойства параметров службы удаленных рабочих столов
- Свойство параметров службы удаленных рабочих столов, интерфейс Иремотедесктопклиент
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиент, свойство Settings
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988939"
---
# <a name="iremotedesktopclientsettings-property"></a>Свойство Иремотедесктопклиент:: Settings

Извлекает объект параметров для клиента контейнера приложения протокол удаленного рабочего стола (RDP).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Значение свойства

Объект параметров для клиента RDP.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ иремотедесктопклиент определен как 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иремотедесктопклиент**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

