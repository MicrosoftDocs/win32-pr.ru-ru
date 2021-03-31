---
title: Создание групп в домене
description: Объект группы создается в службах домен Active Directory в контейнере домена, где будет содержаться новая группа.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- группы AD, создание групп в домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069794"
---
# <a name="creating-groups-in-a-domain"></a>Создание групп в домене

Объект группы создается в службах домен Active Directory в контейнере домена, где будет содержаться новая группа. Группы можно создавать в корне домена, в подразделении или в контейнере. Чтобы создать объект группы, используйте метод [**иадсконтаинер:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) или [**Идиректорйобжект:: креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

Следующие атрибуты необходимы для того, чтобы сделать объект группы юридическим группой, которую будет распознать сервер Active Directory и система безопасности Windows:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**CN**
</dt> <dd>

Указывает имя объекта группы в каталоге. Это будет относительное различающееся имя объекта в контейнере, в котором создается группа.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

Содержит целое число, указывающее тип и область действия группы. Перечисление перечисления [**\_ \_ типов \_ групп ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) определяет возможные значения для атрибута **groupType** .

В следующем списке определяются общие типы групп и значения для этого атрибута.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Локальное распределение домена
</dt> <dd>

**\_Тип группы \_ ADS \_ \_ Локальная \_ группа домена**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Локальная безопасность домена
</dt> <dd>

**Реклама \_ Группа \_ типов групп объявлений \_ \_ локальной \_ группы домена тип** \| **\_ \_ \_ безопасности \_ включена**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Глобальное распределение
</dt> <dd>

**\_ \_ \_ Глобальная \_ группа типов ADS**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Глобальная безопасность
</dt> <dd>

**Реклама \_ Тип группы ADS \_ \_ глобальные \_ группы** \| **баннеры с \_ \_ \_ \_ включенной безопасностью**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Универсальное распределение
</dt> <dd>

**\_ \_ \_ универсальная группа ADS Type Group \_**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Универсальная безопасность
</dt> <dd>

**Реклама \_ Тип \_ группы \_ \_** \| **ADS группа AD с \_ \_ \_ \_ включенной безопасностью**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Если группа предназначена для настройки контроля доступа к объектам каталога, группа должна быть глобальной безопасностью или универсальной группой безопасности.

Имейте в виду, что универсальные группы безопасности можно создавать только в доменах Windows 2000, работающих в собственном режиме. Дополнительные сведения об обнаружении смешанного и собственного режимов см. [в разделе Обнаружение режима работы домена](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**
</dt> <dd>

Содержит строку, которая является именем, используемым для поддержки клиентов и серверов из предыдущей версии. Для поддержки клиентов предыдущей версии Windows значение **SamAccountName** должно быть меньше 20 символов.

Значение **SamAccountName** должно быть уникальным для всех объектов субъекта безопасности в домене. Для проверки уникальности **SamAccountName** в домене необходимо выполнить запрос к домену.

</dd> </dl>

Элементы группы можно добавить во время создания с помощью метода [**идиректорйобжект:: креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . При необходимости члены можно добавить в группу после создания с помощью метода [**иадсграуп:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Дополнительные сведения о добавлении членов в группу см. в разделе [Добавление членов в группы в домене](adding-members-to-groups-in-a-domain.md).

 

 