---
title: Метод Ивмвиртуалмачинивентс Оненханцедвидеомодечанжед (Впккоминтерфацес. h)
description: Получает уведомление о том, что изменилась поддержка виртуальной машины для расширенного видеорежима.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Метод Оненханцедвидеомодечанжед Virtual PC
- Метод Оненханцедвидеомодечанжед Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Оненханцедвидеомодечанжед
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bcdee9db2cf4b37b40d0cc77d6592c5ca1552b0a59642a01c2fe84bf4f69f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056622"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>Метод Ивмвиртуалмачинивентс:: Оненханцедвидеомодечанжед

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что изменилась поддержка виртуальной машины для расширенного видеорежима.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*енханцедвидеомоде* \[ окне\]
</dt> <dd>

Указывает, доступен ли расширенный видеорежим.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачинивентс**](ivmvirtualmachineevents.md)
</dt> </dl>

 

