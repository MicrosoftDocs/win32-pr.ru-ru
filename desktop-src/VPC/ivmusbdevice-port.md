---
title: Свойство порта Ивмусбдевице (Впккоминтерфацес. h)
description: Возвращает идентификатор порта, к которому подключено устройство.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Свойство порта Virtual PC
- Свойство порта Virtual PC, интерфейс Ивмусбдевице
- Интерфейс Ивмусбдевице Virtual PC, свойство Port
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803580"
---
# <a name="ivmusbdeviceport-property"></a>Ивмусбдевице: свойство порт:P

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает идентификатор порта, к которому подключено устройство.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a>Значение свойства

Идентификатор порта. Это значение назначается драйвером соединителя USB.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                            | Значение                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>               | Метод завершился успешно.<br/> |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl> | Параметр имеет **значение NULL**.<br/>         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмусбдевице определяется как 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмусбдевице**](ivmusbdevice.md)
</dt> </dl>

 

