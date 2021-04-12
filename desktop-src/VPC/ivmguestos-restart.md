---
title: Метод Restart Ивмгуестос (Впккоминтерфацес. h)
description: Перезапускает операционную систему на виртуальной машине.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Метод Restart Virtual PC
- Метод Restart Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Restart
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415628"
---
# <a name="ivmguestosrestart-method"></a>Метод Ивмгуестос:: Restart

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Перезапускает операционную систему на виртуальной машине.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

не *принудительно* \[ окне\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если требуется Принудительная перезагрузка, и значение **Variant \_ false** в противном случае.

</dd> <dt>

*аутрестарттаск* \[ out, retval\]
</dt> <dd>

Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания хода выполнения последовательности перезапуска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Возвращаемый код и значение                                                                                                                                                                    | Описание                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> <dt>0</dt> </dl>                                          | Операция выполнена успешно.<br/>                                   |
| <dl> <dt>**Д \_**</dt> <dt>0x80004003</dt> указателя </dl>                            | Параметр *аутрестарттаск* имеет **значение NULL**.<br/>                     |
| <dl> <dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt> </dl>                    | Произошла непредвиденная ошибка.<br/>                               |
| <dl> <dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt> </dl>                     | Операция не завершилась своевременно.<br/>              |
| <dl> <dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt> </dl>               | Для этой операции должна быть запущена виртуальная машина (ВМ).<br/>    |
| <dl> <dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt> </dl>                    | Конфигурация неизвестна.<br/>                                   |
| <dl> <dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt> </dl> | Компонент интеграции компонентов не установлен на этой виртуальной машине.<br/> |



 

## <a name="remarks"></a>Комментарии

Следующие значения можно возвратить с помощью свойства [**Error**](ivmtask-error.md) возвращенного объекта [**ивмтаск**](ivmtask.md) .



| Код [**ошибки**](ivmtask-error.md) /значение                                                                                                                                                                                                                                                                          | Описание                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005<br/>                             | Вызывающий объект должен иметь разрешения на выполнение для этой виртуальной машины.<br/>             |
| <span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)<br/>                         | Компьютер заблокирован и не может завершить работу без параметра Force.<br/> |
| <span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)<br/>                                             | Устройство не готово.<br/>                                                 |
| <span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)<br/> | Выполняется завершение работы системы.<br/>                                        |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

