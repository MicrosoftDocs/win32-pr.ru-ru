---
description: Описывает ошибки поставщика WMI SNMP с 221 по 230.
ms.assetid: 50ca7a6b-2367-464b-98af-b65b0fab42c4
ms.tgt_platform: multiple
title: Ошибки с 221 по 230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e250430efb20af40445e11a67059a31c838eb36ddfb57b1d3d52e29e66074b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131426"
---
# <a name="errors-221-through-230"></a>Ошибки с 221 по 230

Описывает ошибки поставщика WMI SNMP с 221 по 230.

[Неустранимая ошибка 222](#fatal-error-222)

[Неустранимая ошибка 223](#fatal-error-223)

[Неустранимая ошибка 224](#fatal-error-224)

[Неустранимая ошибка 225](#fatal-error-225)

[Неустранимая ошибка 226](#fatal-error-226)

[Неустранимая ошибка 227](#fatal-error-227)

[Неустранимая ошибка 228](#fatal-error-228)

[Неустранимая ошибка 229](#fatal-error-229)

[Предупреждение 230](#warning-230)

## <a name="fatal-error-222"></a>Неустранимая ошибка 222

<dl> <dt>

<span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222, Неустранимая>: " <fileName> : <line \#>: уведомление-тип не разрешен в с поддержкой SMI"**
</dt> <dd>

Ошибка синтаксиса модуля. Вы использовали тип уведомления SNMPv2C в базе MIB, но указали параметр **/v1** , для которого требуется строгое соответствие синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-223"></a>Неустранимая ошибка 223

<dl> <dt>

<span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223, Неустранимая>: " <fileName> : <line \#>: модуль — удостоверение не разрешено в соответствии с SMI**
</dt> <dd>

Ошибка синтаксиса модуля. Вы использовали УДОСТОВЕРЕНие модуля для SNMPv2C в базе данных MIB, но указали параметр **/v1** , который требует более тщательного соответствия синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-224"></a>Неустранимая ошибка 224

<dl> <dt>

<span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224, Неустранимая>: " <fileName> : <line \#>: объект — удостоверение не разрешено в" No/с SMI "**
</dt> <dd>

Ошибка синтаксиса модуля. В базе данных MIB использовался идентификатор объекта, зависящий от SNMPv2C, но был указан параметр **/v1** , что требует более тщательного соответствия синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-225"></a>Неустранимая ошибка 225

<dl> <dt>

<span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225, Неустранимая>: " <fileName> : <line \#>: ТЕКСТОВОЕ-соглашение не разрешено в стандарте SMI"**
</dt> <dd>

Ошибка синтаксиса модуля. Вы использовали ТЕКСТОВОЕ соглашение SNMPv2C в базе MIB, но указали параметр **/v1** , который требует более тщательного соответствия синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-226"></a>Неустранимая ошибка 226

<dl> <dt>

<span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226, Неустранимая>: " <fileName> : <строка \#>: объект — группа не разрешена в соответствии с SMI**
</dt> <dd>

Ошибка синтаксиса модуля. Вы использовали группу объектов SNMPv2C в базе MIB, но указали параметр **/v1** , что требует более тщательного соответствия синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-227"></a>Неустранимая ошибка 227

<dl> <dt>

<span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227, Неустранимая>: " <fileName> : <line \#>: уведомление-группа не разрешена в соответствии с SMI"**
</dt> <dd>

Ошибка синтаксиса модуля. Вы использовали группу уведомлений SNMPv2C в базе MIB, но указали параметр **/v1** , который требует более тщательного соответствия синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-228"></a>Неустранимая ошибка 228

<dl> <dt>

<span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228, Неустранимая>: " <fileName> : <line \#>: соответствие модуля не разрешено в политике SMI"**
</dt> <dd>

Ошибка синтаксиса модуля. В MIB использовался модуль, зависящий от SNMPv2C, но был указан параметр **/v1** , для которого требуется более тщательное соответствие синтаксису в стандарте.

</dd> </dl>

## <a name="fatal-error-229"></a>Неустранимая ошибка 229

<dl> <dt>

<span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229, Неустранимая>: " <fileName> : <line \#>:" возможности агента не разрешены в "без поддержки SMI"**
</dt> <dd>

Ошибка синтаксиса модуля. Вы использовали возможности агента, относящиеся к SNMPv2C, в базе MIB, но указали параметр **/v1** , который требует более тщательного соответствия синтаксису в стандарте.

</dd> </dl>

## <a name="warning-230"></a>Предупреждение 230

<dl> <dt>

<span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, предупреждение>: " <fileName> : <line \#>:" <the wrong token> "используется. Предполагается ":: =" "**
</dt> <dd>

Вместо ":: =" использовался токен ": =", "::" или "=".

</dd> </dl>

 

 



