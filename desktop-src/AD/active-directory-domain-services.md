---
title: Доменные службы Active Directory
description: Службы Microsoft домен Active Directory Services являются основой для распределенных сетей, построенных на базе Windows 2000 Server, Windows Server 2003 и Microsoft Windows Server 2008, которые используют контроллеры домена.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Службы домен Active Directory Active Directory
- Active Directory Active Directory, начальная страница
- Active Directory домен Active Directory Services, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070824"
---
# <a name="active-directory-domain-services"></a>Доменные службы Active Directory

## <a name="purpose"></a>Назначение

Службы Microsoft домен Active Directory Services являются основой для распределенных сетей, построенных на базе Windows 2000 Server, Windows Server 2003 и Microsoft Windows Server 2008, которые используют контроллеры домена. Домен Active Directory Services предоставляют безопасное, структурированное, иерархическое хранилище данных для объектов в сети, таких как пользователи, компьютеры, принтеры и службы. Службы домен Active Directory предоставляют поддержку для поиска этих объектов и работы с ними.

В этом разделе представлен обзор служб домен Active Directory и примеры кода для основных задач, таких как поиск объектов и чтение свойств, в более сложные задачи, такие как публикация службы.

Windows 2000 Server и более поздние операционные системы предоставляют пользователям пользовательский интерфейс для работы с объектами и данными в службах домен Active Directory Services. В этом руководство описывается, как расширить и настроить этот пользовательский интерфейс. В нем также описывается расширение служб домен Active Directory путем определения новых классов и атрибутов объектов.

> [!Note]  
> Следующая документация предназначена для компьютерных программистов. Если вы являетесь конечным пользователем, пытающимся выполнить отладку ошибки печати или проблемы с домашней сетью, см. [форумы сообщества Майкрософт](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Где применимо

Сетевые администраторы пишут сценарии и приложения, обращающиеся к службам домен Active Directory для автоматизации общих административных задач, таких как добавление пользователей и групп, Управление принтерами и настройка разрешений для сетевых ресурсов.

Независимые поставщики программного обеспечения и разработчики конечных пользователей могут использовать программирование служб домен Active Directory Services для включения в каталог своих продуктов и приложений. Службы могут публиковать себя в домен Active Directory Services; Клиенты могут использовать службы домен Active Directory для поиска служб, и они могут использовать службы домен Active Directory для поиска и работы с другими объектами в сети.

## <a name="developer-audience"></a>Аудитория разработчиков

Приложения, обращающиеся к данным в службах домен Active Directory Services, могут быть написаны с помощью API [интерфейсов служб Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , API [протокола упрощенного доступа к каталогам](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) или пространства имен [System. DirectoryServices](/dotnet/api/system.directoryservices) .

## <a name="run-time-requirements"></a>Требования к среде выполнения

Службы домен Active Directory работают на контроллерах домена Windows 2000 и более поздних версий. Однако клиентские приложения могут быть написаны для и запускаться в Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 и Windows 95.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[Сведения о службах домен Active Directory](about-active-directory-domain-services.md)
</dt> <dd>

Общие сведения о службах домен Active Directory.

</dd> <dt>

[Использование доменных служб Active Directory](using-active-directory-domain-services.md)
</dt> <dd>

Руководством по программированию служб домен Active Directory Services.

</dd> <dt>

[Справочник по службам домен Active Directory](active-directory-domain-services-reference.md)
</dt> <dd>

Справочник по программированию домен Active Directory Services.

</dd> </dl>

 

 