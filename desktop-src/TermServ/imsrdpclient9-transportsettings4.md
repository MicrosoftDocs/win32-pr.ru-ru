---
title: IMsRdpClient9 TransportSettings4, свойство
description: Извлекает объект, который поддерживает интерфейс IMsRdpClientTransportSettings4.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства TransportSettings4
- Службы удаленных рабочих столов свойства TransportSettings4, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство TransportSettings4
- Службы удаленных рабочих столов свойства TransportSettings4, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство TransportSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340380"
---
# <a name="imsrdpclient9transportsettings4-property"></a>Свойство IMsRdpClient9:: TransportSettings4

Извлекает объект, который поддерживает интерфейс [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на интерфейс [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | \_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> \_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> IID \_ IMsRdpClient9 определен как 28904001-04B6-436C-A55B-0AF1A0883DC9<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





