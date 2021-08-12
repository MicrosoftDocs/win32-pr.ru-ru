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
ms.openlocfilehash: 0580adb49306397460bd99b0135a13956d01b0a839b72e0ae8ae19f00f7c929e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593147"
---
# <a name="ivmtaskcancel-method"></a>Метод Ивмтаск:: Cancel

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмтаск определен как ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмтаск**](ivmtask.md)
</dt> </dl>

 

