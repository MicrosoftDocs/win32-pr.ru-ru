---
title: Имсрдпклиентшелл Исремотепрограмклиентинсталлед, свойство
description: Получает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp в Windows Server 2008 R2.
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
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135503"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Свойство Имсрдпклиентшелл:: Исремотепрограмклиентинсталлед

Получает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp в Windows Server 2008 R2.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Значение свойства

Возвращает значение, указывающее, поддерживает ли клиент подключение к удаленному рабочему столу (RDC) функции RemoteApp.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпклиентшелл определен как d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиентшелл**](imsrdpclientshell.md)
</dt> </dl>

 

 





