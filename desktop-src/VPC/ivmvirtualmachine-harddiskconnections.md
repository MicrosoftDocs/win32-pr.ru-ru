---
title: Свойство Харддискконнектионс Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию подключений к жестким дискам.
ms.assetid: 167eb8af-bbc1-49a8-83fd-8d946b50530d
keywords:
- Харддискконнектионс свойство Virtual PC
- Харддискконнектионс свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Харддискконнектионс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HardDiskConnections
- IVMVirtualMachine.get_HardDiskConnections
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4a409337dc6fb437a98fe002f6e0d5d4da44b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802686"
---
# <a name="ivmvirtualmachineharddiskconnections-property"></a>Свойство Ивмвиртуалмачине:: Харддискконнектионс

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает перечисляемую коллекцию подключений к жестким дискам.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_HardDiskConnections(
  [out, retval] IVMHardDiskConnectionCollection **hardDiskConnectionCollection
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмхарддискконнектионколлектион**](ivmharddiskconnectioncollection.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация неизвестна.<br/>     |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачине**](ivmvirtualmachine.md)
</dt> </dl>

 

