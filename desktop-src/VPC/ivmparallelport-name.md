---
title: Свойство имени Ивмпараллелпорт (Впккоминтерфацес. h)
description: Имя параллельного порта.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмпараллелпорт
- Ивмпараллелпорт интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135038"
---
# <a name="ivmparallelportname-property"></a>Свойство Ивмпараллелпорт:: Name

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает и задает имя параллельного порта.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a>Значение свойства

Задает имя параллельного порта (например, «LPT1»).

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>                              |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>                                 |
| <dl> <dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | Параметр ссылается на недопустимый параллельный порт.<br/> |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Недопустимая конфигурация для этой виртуальной машины.<br/>   |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                          |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмпараллелпорт определен как 097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмпараллелпорт**](ivmparallelport.md)
</dt> </dl>

 

