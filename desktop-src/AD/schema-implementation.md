---
title: Реализация схемы
description: В домен Active Directory Services определения классов и атрибутов хранятся в каталоге как экземпляры классов classSchema и attributeSchema соответственно.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025022"
---
# <a name="schema-implementation"></a>Реализация схемы

В домен Active Directory Services определения классов и атрибутов хранятся в каталоге как экземпляры классов [**classSchema**](/windows/desktop/ADSchema/c-classschema) и [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) соответственно. **classSchema** и **attributeSchema** — это классы, определенные в схеме. Для работы со схемой Active Directory используйте те же операции LDAP, которые используются для работы с другим объектом. Поскольку схема является ключевой частью каталога, влияющего на весь лес, к расширениям схемы применяются специальные ограничения. Дополнительные сведения об ограничениях см. [в разделе ограничения на расширения схемы](restrictions-on-schema-extension.md).

Для суммирования реализации схемы:

-   Экземпляры класса [**classSchema**](/windows/desktop/ADSchema/c-classschema) определяют каждый класс объектов, поддерживаемый службами домен Active Directory. Атрибуты объекта **classSchema** , например его атрибуты [**mayContain**](/windows/desktop/ADSchema/a-maycontain) и [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) , описывают класс объекта так же, как атрибуты объекта пользователя, например его атрибуты [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) и [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) , описывают этого пользователя. Дополнительные сведения см. в разделе [характеристики классов объектов](characteristics-of-object-classes.md).
-   Экземпляры класса [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) используются для определения каждого атрибута, поддерживаемого службами домен Active Directory. Атрибуты объекта **attributeSchema** , например атрибуты **attributeSyntax** и **иссинглевалуед** , описывают атрибут так же, как атрибуты пользовательского объекта описывают этого пользователя. Дополнительные сведения см. в разделе [характеристики атрибутов](characteristics-of-attributes.md).
-   Экземпляры классов [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) и [**classSchema**](/windows/desktop/ADSchema/c-classschema) хранятся в хорошо известном месте в каталоге, контейнере схемы. Контейнер схемы всегда имеет различающееся имя формы:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    где " &lt; DC = forestroot &gt; " — это различающееся имя корня леса, например "DC = Fabrikam, DC = com".

    Чтобы получить различающееся имя контейнера схемы, прочитайте атрибут **счеманамингконтекст** в RootDSE. Дополнительные сведения о rootDSE и ее атрибутах см. в разделе [Привязка бессерверных данных и RootDSE](serverless-binding-and-rootdse.md).

При обдумывании схемы Помните:

-   Изменения схемы являются глобальными. Для всего леса существует одна схема. Схема глобально реплицируется: копия схемы существует на каждом контроллере домена в лесу. При расширении схемы это делается для всего леса.
-   Добавление схем необратимо. При добавлении в схему нового класса или атрибута его нельзя удалить. Существующий атрибут или класс можно отключить, но не удалять. Дополнительные сведения см. в разделе [Отключение существующих классов и атрибутов](disabling-existing-classes-and-attributes.md).
-   Отключение класса или атрибута не влияет на существующие экземпляры класса или атрибута, но не позволяет создавать новые экземпляры. Нельзя отключить атрибут, если он включен в любой класс, который не отключен.

 

 