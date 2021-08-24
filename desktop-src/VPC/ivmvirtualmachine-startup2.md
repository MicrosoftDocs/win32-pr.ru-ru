---
title: Метод Ивмвиртуалмачине Startup2 (Впккоминтерфацес. h)
description: Запускает виртуальную машину из неинициализированного или сохраненного состояния с дополнительными параметрами.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Метод Startup2 Virtual PC
- Метод Startup2 Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Startup2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b76364f80d9faaaeeb0f9760ce434d91658afc6699a7acdeee98f0a2e65548d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652894"
---
# <a name="ivmvirtualmachinestartup2-method"></a>Метод Ивмвиртуалмачине:: Startup2

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Запуск виртуальной машины из неинициализированного или сохраненного состояния с дополнительными параметрами.

Этот метод предоставляет механизм для запуска виртуальной машины с разностным диском, даже если изменилась метка времени родительского диска.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стартупоптион* \[ окне\]
</dt> <dd>

Дополнительный параметр запуска. Возможные значения — из перечисления [**вмстартупоптион**](vmstartupoption.md) .

</dd> <dt>

*стартуптаск* \[ out, retval\]
</dt> <dd>

Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности запуска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Возвращаемый код и значение                                                                                                                                                                          | Описание                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> <dt>0</dt> </dl>                                                | Операция выполнена успешно.<br/>                                     |
| <dl> <dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | Недопустимый параметр *стартупоптион* .<br/>                       |
| <dl> <dt>**Д \_**</dt> <dt>0x80004003</dt> указателя </dl>                                  | Параметр *стартуптаск* имеет **значение NULL**.<br/>                          |
| <dl> <dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ \_ отказа в доступе)**</dt> <dt>0x80070005</dt> </dl> | Вызывающий объект должен иметь разрешения на выполнение для запуска этой виртуальной машины.<br/> |
| <dl> <dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt> </dl>                           | Операция не завершилась своевременно.<br/>                |
| <dl> <dt>**Виртуальная машина \_ \_Извлечь \_ из 0xA0040203 \_ ресурсов**</dt> <dt></dt> </dl>                    | Недостаточно ресурсов узла.<br/>                              |
| <dl> <dt>**Виртуальная машина \_ \_Слишком \_ много \_ виртуальных машин**</dt> <dt>0xA0040204</dt> </dl>                       | Слишком много активных виртуальных машин.<br/>                                    |
| <dl> <dt>**Виртуальная машина \_ \_Виртуальная машина E \_ с**</dt> <dt>0xA0040500</dt> </dl>                          | Виртуальная машина уже запущена.<br/>                                        |
| <dl> <dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt> </dl>                          | Произошла непредвиденная ошибка.<br/>                                 |



 

## <a name="remarks"></a>Remarks

Следующие значения можно возвратить с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) .



| Код [**ошибки**](ivmtask-error.md) /значение                                                                                                                                                                                                                                      | Описание                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)<br/>                                                 | Оборудование не поддерживает виртуализацию.<br/>              |
| <span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)<br/> | Виртуализация оборудования отключена.<br/>                       |
| <span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)<br/>                             | установлены виртуальные компьютеры 2007 и Windows virtual pc.<br/> |
| <span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)<br/>             | Установлено другое программное обеспечение виртуализации.<br/>                |
| <span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)<br/>                                                                 | Недостаточно ресурсов узла.<br/>                       |



 

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

 

