---
description: Запрашивает изменение состояния TPM на значение, указанное в параметре Рекуестедтпмстате.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Метод Рекуесттпмстатечанже класса CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991593"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Метод Рекуесттпмстатечанже \_ класса TPM CIM

Запрашивает изменение состояния TPM на значение, указанное в параметре *рекуестедтпмстате* . Если вызов метода завершается успешно, свойство **тпмстате** должно быть равно значению параметра **рекуестедтпмстате** . Вызов метода **рекуесттпмстатечанже** несколько раз может привести к перезаписанию или потере более ранних запросов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рекуестедтпмстате* \[ окне\]
</dt> <dd>

Запрошенное состояние доверенного платформенного модуля.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 Enabled — активный — владелец** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**Недоступность S2 — активный — владелец** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 Enabled — неактивно — владелец** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**Состояние S4 отключено — неактивно — владелец** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 включено — активно — не владеет** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 Disabled — активный — не владеет** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 Enabled — Inactive — не владеет** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 Disabled — неактивный — не владеет** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Аусоризатионтокен* \[ окне\]
</dt> <dd>

Токен авторизации, который может потребоваться для вступления в силу действия. Параметр *аусоризатионтокен* может потребоваться для установления физического присутствия или для передачи овнераус, определяемого TCG пароля авторизации владельца. В случае с Овнераус может потребоваться шаредкредентиал CIM \_ со значением, отличным от NULL \_ Шаредкредентиал. Secret. Свойство CIM \_ шаредкредентиал. Algorithm также может быть задано на основе свойства CIM \_ Тпмкапабилитиес. суппортедпассвордалгорисмс.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Может содержать ссылку на [**\_ конкретежоб CIM**](cim-concretejob.md) , созданную для отслеживания перехода состояния, инициированного вызовом метода.

</dd> <dt>

*Тимеаутпериод* \[ окне\]
</dt> <dd>

Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние. Для указания *тимеаутпериод* необходимо использовать формат интервала. Значение 0 или параметр NULL указывает, что у клиента нет требований к времени для перехода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Неизвестная или Неуказанная ошибка** (2)
</dt> <dt>

**Невозможно завершить в течение времени ожидания** (3)
</dt> <dt>

**Сбой** (4)
</dt> <dt>

**Недопустимый параметр** (5)
</dt> <dt>

**Используется** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Недопустимая смена состояния** (4097)
</dt> <dt>

**Использование параметра времени ожидания не поддерживается** (4098)
</dt> <dt>

**Занято** (4099)
</dt> <dt>

**Метод зарезервирован** (4100.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




