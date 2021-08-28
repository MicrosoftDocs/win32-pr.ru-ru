---
title: Атрибуты (AD DS)
description: Каждый объект в домен Active Directory Services содержит набор атрибутов, определяющих характеристики объекта.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- атрибуты AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dba576893c7b48d63ea035d4942ad1c07915814ffb86b6c4f9e4589dc574b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024215"
---
# <a name="attributes-ad-ds"></a>Атрибуты (AD DS)

Каждый объект в домен Active Directory Services содержит набор атрибутов, определяющих характеристики объекта. Каждый атрибут описывается объектом [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) в контейнере схемы, определяющим атрибут. Определение атрибута включает различные данные, например типы объектов, к которым применяется атрибут, и тип синтаксиса атрибута. Дополнительные сведения об определениях схемы атрибутов см. в разделе [характеристики атрибутов](characteristics-of-attributes.md).

В следующем списке перечислены типы атрибутов, которые хранятся в службах домен Active Directory.

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Реплицируемые в домене, сохраненные атрибуты
</dt> <dd>

Некоторые атрибуты хранятся в каталоге (например, [**CN**](/windows/desktop/ADSchema/a-cn), [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)и [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) и реплицируются на все контроллеры домена в домене. Подмножество этих атрибутов также реплицируется в глобальный каталог. При перечислении атрибутов объекта из глобального каталога возвращаются только атрибуты, реплицированные в глобальный каталог. Некоторые атрибуты также индексируются, поскольку включение индексированного свойства в запрос повышает производительность запросов.

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Нереплицированные, локально сохраненные атрибуты
</dt> <dd>

Нереплицированные атрибуты, такие как [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-logon**](/windows/desktop/ADSchema/a-lastlogon)и [**Last-logoff**](/windows/desktop/ADSchema/a-lastlogoff) , хранятся на каждом контроллере домена, но не реплицируются. Нереплицированные атрибуты — это атрибуты, относящиеся к конкретному контроллеру домена. Например, атрибут **последнего входа** — это последняя Дата и время проверки сетевого входа пользователя на конкретный контроллер домена, который вернул это свойство. Эти атрибуты могут быть получены таким же образом, как и атрибуты на уровне домена, описанные выше. Однако для этих атрибутов каждый контроллер домена хранит только значения, относящиеся к конкретному контроллеру домена. Например, чтобы получить сведения о последнем входе пользователя в домен, извлеките атрибут **последнего входа** пользователя из каждого контроллера домена в домене и найдите последнюю дату и время.

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Несохраненные, сконструированные атрибуты
</dt> <dd>

Объект пользователя также имеет сконструированные атрибуты, которые не хранятся в каталоге, но вычисляются контроллером домена, например [**каноникалнаме**](/windows/desktop/ADSchema/a-canonicalname) и [**алловедаттрибутес**](/windows/desktop/ADSchema/a-allowedattributes).

</dd> </dl>

 

 