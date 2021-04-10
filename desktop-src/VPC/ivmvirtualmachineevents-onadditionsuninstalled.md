---
title: Метод Ивмвиртуалмачинивентс Онаддитионсунинсталлед (Впккоминтерфацес. h)
description: Получает уведомление об удалении компонентов интеграции на виртуальной машине.
ms.assetid: bbbc01b6-adb1-491e-a5b0-ff463dca7dfd
keywords:
- Метод Онаддитионсунинсталлед Virtual PC
- Метод Онаддитионсунинсталлед Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онаддитионсунинсталлед
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsUninstalled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 514a88249ad34d51965df75feab6f129bd9fa5a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135034"
---
# <a name="ivmvirtualmachineeventsonadditionsuninstalled-method"></a>Метод Ивмвиртуалмачинивентс:: Онаддитионсунинсталлед

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление об удалении компонентов интеграции на виртуальной машине.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnAdditionsUninstalled();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачинивентс**](ivmvirtualmachineevents.md)
</dt> </dl>

 

