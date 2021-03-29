---
title: Свойство график Ивмаккаунтант (Впккоминтерфацес. h)
description: Получение процента текущей загрузки ЦП для этой виртуальной машины.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- График свойство Virtual PC
- График свойство Virtual PC, интерфейс Ивмаккаунтант
- Ивмаккаунтант интерфейс Virtual PC, свойство график
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989314"
---
# <a name="ivmaccountantcpuutilization-property"></a>Свойство Ивмаккаунтант:: график

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получение процента текущей загрузки ЦП для этой виртуальной машины.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>Значение свойства

Процент текущей загрузки ЦП.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>       |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>          |
| <dl> <dt>С \_ ЛОЖЬ</dt> <dt>1</dt> </dl>                    | Виртуальная машина не запущена.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмаккаунтант определен как 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмаккаунтант**](ivmaccountant.md)
</dt> </dl>

 

