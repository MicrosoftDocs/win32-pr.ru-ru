---
title: Свойство типа Ивмсериалпорт (Впккоминтерфацес. h)
description: Возвращает тип последовательного порта.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Тип свойства Virtual PC
- Тип свойства Virtual PC, интерфейс Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, тип Property
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eee02721152bd75ffa39a802de0b49ac7878e9a05335217c656fc64ad4ff55a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973854"
---
# <a name="ivmserialporttype-property"></a>Свойство Ивмсериалпорт:: Type

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает тип последовательного порта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a>Значение свойства

Тип последовательного порта. Список значений см. в разделе [**вмсериалпорттипе**](vmserialporttype.md).

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>                            |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет значение NULL.<br/>                                   |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Недопустимая конфигурация для этой виртуальной машины.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмсериалпорт**](ivmserialport.md)
</dt> </dl>

 

