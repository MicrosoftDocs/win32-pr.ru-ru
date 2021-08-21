---
title: Свойство Биоссериалнумбер Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Серийный номер BIOS.
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- Биоссериалнумбер свойство Virtual PC
- Биоссериалнумбер свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Биоссериалнумбер
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f5cbf848f35cda387b1f596e68a7316e99cc7392c2c8c93c806186b961b37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123184"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a>Свойство Ивмвиртуалмачине:: Биоссериалнумбер

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает и устанавливает серийный номер BIOS.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a>Значение свойства

Указывает серийный номер BIOS.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                               | Значение                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                  | Операция выполнена успешно.<br/>                                               |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>                    | Параметр имеет **значение NULL**.<br/>                                                  |
| <dl> <dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | Значение параметра больше 32 символов, пустая строка или недопустимо.<br/> |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl>            | Конфигурация неизвестна.<br/>                                               |
| <dl> <dt>Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным</dt> <dt>0xA004020B</dt> </dl> | Виртуальная машина находится в работающем или сохраненном состоянии.<br/>                         |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>            | Произошла непредвиденная ошибка.<br/>                                           |



## <a name="remarks"></a>Remarks

Это свойство не будет содержать действительные сведения до тех пор, пока виртуальная машина не запустится в первый раз. При считывании перед начальным запуском будет возвращена пустая строка.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмвиртуалмачине**](ivmvirtualmachine.md)
</dt> </dl>

 

