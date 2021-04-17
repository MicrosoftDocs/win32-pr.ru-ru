---
description: Запрашивает изменение состояния запланированной системы на указанное значение.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Метод RequestStateChange класса Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683377"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a>Метод RequestStateChange \_ класса мсвм планнедкомпутерсистем

Запрашивает изменение состояния запланированной системы на указанное значение.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RequestedState* \[ окне\]
</dt> <dd>

Запрошенное состояние для запланированной системы.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Завершение работы** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Вне сети** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Тест** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Отложить** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Замораживание** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Перезагрузка** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Сброс** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Этот параметр не используется и должен иметь **значение NULL**.

</dd> <dt>

*Тимеаутпериод* \[ окне\]
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.



| Возвращаемый код и значение                                                                                                                      | Описание                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>0</dt> </dl>     | Успешно<br/>                                                                 |
| <dl> <dt></dt><dt>4096</dt> </dl>  |                                                                                    |
| <dl> <dt></dt><dt>32768</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32769</dt> </dl> | Доступ запрещен.<br/>                                                          |
| <dl> <dt></dt><dt>32770</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32771</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32772</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32773</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32774</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32775</dt> </dl> | Значение, указанное в параметре *RequestedState* , не поддерживается.<br/> |
| <dl> <dt></dt><dt>32776</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32777</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32778</dt> </dl> |                                                                                    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




