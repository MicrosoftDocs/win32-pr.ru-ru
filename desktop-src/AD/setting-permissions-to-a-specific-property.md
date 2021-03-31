---
title: Установка разрешений для определенного свойства
description: Разрешения можно задать для применения к определенному свойству объекта.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Установка разрешений для конкретного свойства Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069743"
---
# <a name="setting-permissions-to-a-specific-property"></a>Установка разрешений для определенного свойства

Разрешения можно задать для применения к определенному свойству объекта.

**Установка разрешений, относящихся к определенному свойству объекта**

1.  Задайте для свойства [**иадсакцессконтролентри. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **ADS \_ справа \_ DS \_ Read \_ prop** и/или **ADSS \_ right \_ DS- \_ \_ prop**.
2.  Задайте для свойства [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.
3.  Присвойте свойству [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **schemaIDGUID** свойства. Это **schemaIDGUID** объекта **attributeSchema** , определяющего свойство в схеме. Идентификатор GUID должен быть указан в виде строки формы, созданной функцией [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) в библиотеке COM.
4.  Присвойте параметру [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **\_ \_ \_ тип \_ объекта флага ADS**.

Дополнительные сведения о **schemaIDGUID** предопределенного атрибута см. в разделе [Справочник по службам домен Active Directory](active-directory-domain-services-reference.md).

Дополнительные сведения и пример кода, который можно использовать для получения schemaIDGUID, см. в разделе [чтение объектов attributeSchema и classSchema](reading-attributeschema-and-classschema-objects.md).

Дополнительные сведения о создании элемента управления доступом см. в разделе [Установка прав доступа для объекта](setting-access-rights-on-an-object.md).

Дополнительные сведения и пример кода, который можно использовать для задания ACE, относящегося к конкретному свойству, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 