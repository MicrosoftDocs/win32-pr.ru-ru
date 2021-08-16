---
title: Свойство мыши Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает устройство мыши для виртуальной машины.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Виртуальный ПК свойства мыши
- Свойство мыши Virtual PC, интерфейс Ивмвиртуалмачине
- Интерфейс Ивмвиртуалмачине Virtual PC, свойство Mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ef16d32410e66e8ea3a3baf23160074cf99d97762df3402bf437d0719d6332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344658"
---
# <a name="ivmvirtualmachinemouse-property"></a>Ивмвиртуалмачине:: Mouse, свойство

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает устройство мыши для виртуальной машины.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивммаусе**](ivmmouse.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                         | Значение                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                            | Операция выполнена успешно.<br/>       |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>              | Параметр имеет **значение NULL**.<br/>          |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl>      | Конфигурация неизвестна.<br/>       |
| <dl> <dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt> </dl> | Виртуальная машина не запущена.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>      | Произошла непредвиденная ошибка.<br/>   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачине**](ivmvirtualmachine.md)
</dt> </dl>

 

