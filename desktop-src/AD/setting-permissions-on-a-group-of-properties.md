---
title: Установка разрешений для группы свойств
description: Разрешения могут быть применены к группе свойств.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Установка разрешений для группы свойств Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a50fa74cd39353170089bc39940b7bc063e8c94454d46c50bf14a1fa0a9edee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183423"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>Установка разрешений для группы свойств

Разрешения могут быть применены к группе свойств. Набор свойств определяется идентификатором GUID в атрибуте [**ригхтсгуид**](/windows/desktop/ADSchema/a-rightsguid) объекта [**контролакцессригхт**](/windows/desktop/ADSchema/c-controlaccessright) . Этот идентификатор GUID задается в атрибуте [**аттрибутесекуритигуид**](/windows/desktop/ADSchema/a-attributesecurityguid) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) каждого атрибута в группе.

В следующей процедуре показано, как задать разрешения, которые применяются к группе свойств объекта.

**Установка разрешений, относящихся к группе свойств объекта**

1.  Задайте для свойства [**иадсакцессконтролентри. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **ADS \_ справа \_ DS redirectory \_ Read \_ prop**, **AD \_ right \_ DS \_ запись \_ prop** или оба значения вместе.
2.  Задайте для свойства [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.
3.  Задайте для свойства [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) идентификатор GUID набора свойств. Это свойство [**ригхтсгуид**](/windows/desktop/ADSchema/a-rightsguid) объекта [**контролакцессригхт**](/windows/desktop/ADSchema/c-controlaccessright) , идентифицирующее набор свойств. Этот GUID также задается как [**аттрибутесекуритигуид**](/windows/desktop/ADSchema/a-attributesecurityguid) в объекте attributeSchema каждого свойства в группе.
4.  Установите для свойства [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **\_ \_ тип объекта \_ \_ флага ADS**.

Имейте в виду, что не следует задавать **флаг \_ \_ \_ \_ доступа к AD right DS Control** в свойстве [**иадсакцессконтролентри. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) . Этот флаг используется только для указания права доступа к элементу управления.

Дополнительные сведения и пример кода, который можно использовать для установки прав доступа для набора свойств, см. в разделе [пример кода для настройки разрешений для группы свойств](example-code-for-setting-permissions-on-a-group-of-properties.md).

Дополнительные сведения о создании записи ACE см. [в разделе Установка прав доступа для объекта](setting-access-rights-on-an-object.md).

Дополнительные сведения и пример кода, который можно использовать для установки ACE для набора свойств, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 