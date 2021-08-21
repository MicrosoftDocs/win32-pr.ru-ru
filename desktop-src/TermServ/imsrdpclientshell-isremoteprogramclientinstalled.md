---
title: Имсрдпклиентшелл Исремотепрограмклиентинсталлед, свойство
description: возвращает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Исремотепрограмклиентинсталлед
- Службы удаленных рабочих столов свойства Исремотепрограмклиентинсталлед, интерфейс Имсрдпклиентшелл
- Службы удаленных рабочих столов интерфейса Имсрдпклиентшелл, свойство Исремотепрограмклиентинсталлед
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3073bb9a9e5890ff7a6a46bb9ea0c03964bf54f1c91550dbb2746385a11fa809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129767"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Свойство Имсрдпклиентшелл:: Исремотепрограмклиентинсталлед

возвращает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp Windows Server 2008 R2.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Значение свойства

Возвращает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпклиентшелл определен как d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиентшелл**](imsrdpclientshell.md)
</dt> </dl>

 

 





