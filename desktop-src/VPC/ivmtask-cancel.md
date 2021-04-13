---
title: Метод Cancel Ивмтаск (Впккоминтерфацес. h)
description: Отменяет задачу.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Отмена метода Virtual PC
- Отмена метода Virtual PC, интерфейс Ивмтаск
- Интерфейс Ивмтаск Virtual PC, метод Cancel
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341235"
---
# <a name="ivmtaskcancel-method"></a>Метод Ивмтаск:: Cancel

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Отменяет задачу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Возвращаемый код и значение                                                                                                                                                 | Описание                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt> </dl>            | Задачу нельзя отменить.<br/>      |
| <dl> <dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмтаск**](ivmtask.md)
</dt> </dl>

 

