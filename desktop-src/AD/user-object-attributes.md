---
title: Атрибуты объекта «пользователь»
description: Объект пользователя имеет несколько атрибутов. В этом разделе описываются ключевые атрибуты, используемые Windows, средства администрирования и адресная книга Windows (WAB). Он не описывает все атрибуты. для объекта User не используются многие атрибуты.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Атрибуты объекта пользователя AD
- Пользователи AD, атрибуты объектов пользователя
- Объекты AD, пользователь, атрибуты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987303"
---
# <a name="user-object-attributes"></a>Атрибуты объекта «пользователь»

Объект пользователя имеет несколько атрибутов. В этом разделе описываются ключевые атрибуты, используемые Windows, средства администрирования и адресная книга Windows (WAB). Он не описывает все атрибуты. для объекта User не используются многие атрибуты.

Некоторые атрибуты хранятся в каталоге, например [**CN**](/windows/desktop/ADSchema/a-cn), [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)и т. д., и реплицируются на все контроллеры домена в домене. Подмножество этих атрибутов также реплицируется в глобальный каталог.

Нереплицированные атрибуты хранятся на каждом контроллере домена, но не реплицируются в других местах, таких как [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**ластлогон**](/windows/desktop/ADSchema/a-lastlogon), [**ластлогофф**](/windows/desktop/ADSchema/a-lastlogoff)и т. д. Нереплицированные атрибуты — это атрибуты, относящиеся к конкретному контроллеру домена. Например, **ластлогон** — это последняя Дата и время проверки сетевого входа пользователя на конкретный контроллер домена, который возвращает свойство.

Объект пользователя также имеет сконструированные атрибуты, которые не хранятся в каталоге, но вычисляются контроллером домена, например [**каноникалнаме**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**алловедаттрибутес**](/windows/desktop/ADSchema/a-allowedattributes)и т. д.

Атрибуты для пользовательских объектов классифицируются следующим образом:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Атрибуты базового объекта
</dt> <dd>

Эта категория содержит атрибуты, необходимые для всех объектов каталога, таких как [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)и т. д.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Атрибуты именования
</dt> <dd>

В эту категорию входят атрибуты, используемые для обращения к объекту или его указания, такие как [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid)и т. д. Дополнительные сведения об именовании атрибутов для объектов User см. в разделе [атрибуты именования пользователей](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Атрибуты безопасности
</dt> <dd>

В эту категорию входят атрибуты для входа и контроля доступа. Дополнительные сведения об атрибутах безопасности для объектов User см. в разделе [атрибуты безопасности пользователя](security-properties.md).

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Атрибуты адресной книги
</dt> <dd>

Эта категория включает атрибуты для электронной почты и пользовательских данных. Дополнительные сведения об атрибутах адресной книги для объектов User см. в разделе [атрибуты адресной книги пользователя](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Атрибуты конкретного приложения
</dt> <dd>

В эту категорию входят пользовательские данные конфигурации для конкретных приложений.

</dd> </dl>

Дополнительные сведения о чтении и изменении атрибутов объекта пользователя см. в разделе [чтение и запись атрибутов объектов в домен Active Directory Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Дополнительные сведения о классе User, включая полный список атрибутов [**mayContain**](/windows/desktop/ADSchema/a-maycontain) и [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) класса, см. в разделе [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Установка паролей

Пароль пользователя нельзя изменить напрямую, так как это приведет к отправке незашифрованного пароля по сети. Чтобы задать пароль для пользователя, необходимо использовать метод [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) или [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Метод **IADsUser. ChangePassword** используется, когда приложение позволяет пользователю изменить свой пароль. Метод **IADsUser. SetPassword** используется, когда приложение позволяет администратору сбросить пароль.

 

 