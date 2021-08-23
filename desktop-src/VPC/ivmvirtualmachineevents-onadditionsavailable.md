---
title: Метод Ивмвиртуалмачинивентс Онаддитионсаваилабле (Впккоминтерфацес. h)
description: Получает уведомление о том, что компоненты интеграции доступны на виртуальной машине.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- Метод Онаддитионсаваилабле Virtual PC
- Метод Онаддитионсаваилабле Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онаддитионсаваилабле
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81657563a921ca8a9aa7ef511183a56aa2d7a599e69232fcc186d7d911cb65bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056754"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a>Метод Ивмвиртуалмачинивентс:: Онаддитионсаваилабле

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что компоненты интеграции доступны на виртуальной машине.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмвиртуалмачинивентс**](ivmvirtualmachineevents.md)
</dt> </dl>

 

