---
title: Реализация схемы
description: В домен Active Directory Services определения классов и атрибутов хранятся в каталоге как экземпляры классов classSchema и attributeSchema соответственно.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ff18046841b5603be235266e33a7252049f93c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069748"
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

 

 