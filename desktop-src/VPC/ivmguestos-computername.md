---
title: Свойство Ивмгуестос ComputerName (Впккоминтерфацес. h)
description: Имя компьютера гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Свойство ComputerName Virtual PC
- Свойство ComputerName Virtual PC, интерфейс Ивмгуестос
- Интерфейс Ивмгуестос Virtual PC, свойство ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6bb741c0196c79afb758ecd0567c6f334bdd574eb06b901a11e3d48b1efdc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653454"
---
# <a name="ivmguestoscomputername-property"></a>Свойство Ивмгуестос:: ComputerName

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает имя компьютера гостевой операционной системы, работающей на виртуальной машине.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a>Значение свойства

Имя компьютера гостевой операционной системы.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                                       | Значение                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                          | Операция выполнена успешно.<br/>                        |
| <dl> <dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                         | Параметр является недопустимым или не указан.<br/>         |
| <dl> <dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt> </dl>               | Виртуальная машина не запущена.<br/>                               |
| <dl> <dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt> </dl> | Компоненты интеграции не установлены в этой виртуальной машине.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>                    | Произошла непредвиденная ошибка.<br/>                    |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

