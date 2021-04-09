---
title: Свойство ProcessorSpeed Ивмхостинфо (Впккоминтерфацес. h)
description: Скорость хост-процессора в мегагерцах (МГц) или ГГц.
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- ProcessorSpeed свойство Virtual PC
- ProcessorSpeed свойство Virtual PC, интерфейс Ивмхостинфо
- Ивмхостинфо интерфейс Virtual PC, свойство ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc890392db5f61a7819fa1d4b4a11d2b3de312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071069"
---
# <a name="ivmhostinfoprocessorspeed-property"></a>Ивмхостинфо: свойство Роцессорспид:P

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает скорость хост-процессора в мегагерцах (МГц) или ГГц.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a>Значение свойства

Скорость процессора в мегагерцах или в ГГц.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмхостинфо**](ivmhostinfo.md)
</dt> </dl>

 

