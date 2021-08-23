---
title: IMsRdpClientAdvancedSettings6 ПКБ, свойство
description: Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер. | IMsRdpClientAdvancedSettings6 ПКБ, свойство
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство ПКБ
- Службы удаленных рабочих столов свойства ПКБ, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство ПКБ
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68b34a04f99d830b525cadf6e35bc4816d7a52948916dc9a3d54664752dac38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001362"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a>IMsRdpClientAdvancedSettings6::P свойство CB

Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a>Значение свойства

Указывает параметр большого двоичного объекта, который будет использоваться перед подключением.

## <a name="remarks"></a>Remarks

Это свойство поддерживается только клиентами подключение к удаленному рабочему столу 6,1 и 7,0.

Сервер использует параметр большого двоичного объекта для определения целевого процесса для соединения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





