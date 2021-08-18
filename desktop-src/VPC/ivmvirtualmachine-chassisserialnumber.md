---
title: Свойство Чассиссериалнумбер Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Серийный номер корпуса.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Чассиссериалнумбер свойство Virtual PC
- Чассиссериалнумбер свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Чассиссериалнумбер
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40b9922f862e52cc6b1cce3d6f508254f37ca41ec314f4312ffa159cb9cde15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752442"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a>Свойство Ивмвиртуалмачине:: Чассиссериалнумбер

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает и задает серийный номер корпуса.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a>Значение свойства

Указывает серийный номер корпуса.

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмвиртуалмачине**](ivmvirtualmachine.md)
</dt> </dl>

 

