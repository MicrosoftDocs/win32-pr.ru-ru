---
title: Свойство имени Ивмсериалпорт (Впккоминтерфацес. h)
description: Имя последовательного порта.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1862d2fbbecc4cf1efee7b83eb34a1a776f9e3bcc7a1d4949ecb3e5d483dec04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510373"
---
# <a name="ivmserialportname-property"></a>Свойство Ивмсериалпорт:: Name

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает имя последовательного порта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a>Значение свойства

Имя последовательного порта. Например, "COM1" для **вмсериалпорт \_ хостпорт**, "C: \\SerialPort.txt" для **вмсериалпорт \_ TextFile** или " \\ \\ *ServerName* \\ pipe \\ *pipeName*" для **вмсериалпорт \_ помощью канала NamedPipe**.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>                            |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>                               |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Недопустимая конфигурация для этой виртуальной машины.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                        |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмсериалпорт**](ivmserialport.md)
</dt> </dl>

 

