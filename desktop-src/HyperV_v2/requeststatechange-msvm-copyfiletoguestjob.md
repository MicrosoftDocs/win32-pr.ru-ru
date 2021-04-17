---
description: Изменяет состояние задания.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Метод Msvm_CopyFileToGuestJob:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683748"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>Мсвм \_ копифилетогуестжоб:: RequestStateChange, метод

Изменяет состояние задания.

## <a name="syntax"></a>Синтаксис


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RequestedState* \[ окне\]
</dt> <dd>

Новое состояние. Возможные значения:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)


</dt> <dd>

Изменяет состояние на "работает".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)


</dt> <dd>

Временно останавливает задание. Затем клиент может впоследствии перезапустить задание с помощью "Start". Клиент может, возможно, войти в состояние "Service", когда приостановлено (это зависит от задания).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)


</dt> <dd>

Выполнение задания в чистом виде, сохранение данных, сохранение состояния и завершение работы всех базовых процессов в порядке.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)


</dt> <dd>

Помещает задание в состояние службы, зависящее от поставщика. Клиент может, возможно, перезапустить задание.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Тимеаутпериод* \[ окне\]
</dt> <dd>

Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние. Для указания времени ожидания необходимо использовать формат интервала. Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода. Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.



| Возвращаемый код и значение                                                                                                                                                               | Описание                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Завершено без ошибки**</dt> <dt>0</dt> </dl>                   | Успешно.<br/>                                                                |
| <dl> <dt>**Использование параметра времени ожидания не поддерживается**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Сбой**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Отказано в доступе**</dt> <dt>32769</dt> </dl>                         | Доступ запрещен.<br/>                                                          |
| <dl> <dt>**Не поддерживается**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**Состояние неизвестно**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Время ожидания**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Недопустимый параметр**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Система используется**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt> </dl>      | Значение, указанное в параметре *RequestedState* , не поддерживается.<br/> |
| <dl> <dt>**Недопустимый тип данных**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> <dt>**Система недоступна**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Недостаточно памяти**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | \\\\Корневая \\ виртуализация \\ версии 2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ копифилетогуестжоб**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




