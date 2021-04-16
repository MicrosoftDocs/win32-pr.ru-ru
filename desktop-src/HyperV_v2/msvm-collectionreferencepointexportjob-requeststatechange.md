---
description: Запрашивает изменение состояния.
ms.assetid: 34d70ff2-4545-4ab7-8c84-6532c342768b
title: Метод RequestStateChange класса Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a3e8b3f3a7249896f023734d049fa3fa772514f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684271"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Метод RequestStateChange \_ класса мсвм коллектионреференцепоинтекспортжоб

Запрашивает изменение состояния.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RequestedState* \[ окне\]
</dt> <dd>

RequestStateChange изменяет состояние задания. Возможны следующие значения:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)


</dt> <dd>

Изменяет состояние на "работает".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)


</dt> <dd>

Временно останавливает задание. Цель — последующее перезапустить задание с помощью "Start". В приостановленном состоянии можно ввести состояние службы. (Это зависит от задания.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)


</dt> <dd>

Останавливает задание в чистом виде, сохраняет данные, сохраняет состояние и завершает все базовые процессы упорядоченным образом.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)


</dt> <dd>

Помещает задание в состояние службы, зависящее от поставщика. Может быть возможным перезапуск задания.

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

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает одну из следующих ошибок.

<dl> <dt>

  (0)
</dt> <dt>

 (32768)
</dt> <dt>

 (32769)
</dt> <dt>

 (32770)
</dt> <dt>

 (32771)
</dt> <dt>

 (32772)
</dt> <dt>

 (32773)
</dt> <dt>

 (32774)
</dt> <dt>

 (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ коллектионреференцепоинтекспортжоб**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




