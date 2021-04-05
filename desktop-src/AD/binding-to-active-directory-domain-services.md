---
title: Привязка к службам домен Active Directory
description: В домен Active Directory Services работа по сопоставлению программного объекта с конкретным объектом служб домен Active Directory Services называется привязкой.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- Привязка к службам домен Active Directory Active Directory
- Active Directory домен Active Directory Services, привязка к
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990398"
---
# <a name="binding-to-active-directory-domain-services"></a>Привязка к службам домен Active Directory

В домен Active Directory Services работа по сопоставлению программного объекта с конкретным объектом служб домен Active Directory Services называется *привязкой*. Если программный объект, такой как объект [**iAds**](/windows/desktop/api/iads/nn-iads-iads) или [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , связан с конкретным объектом каталога, программный объект считается *привязанным* к объекту каталога.

## <a name="binding-functions-and-methods"></a>Функции и методы привязки

Метод для программной привязки к объекту Active Directory будет зависеть от используемой технологии программирования. Дополнительные сведения о привязке к объектам в домен Active Directory Services с помощью определенной технологии программирования см. в разделах, перечисленных в следующей таблице.



| Технология программирования                                                                       | Дополнительные сведения                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Интерфейсы служб Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Привязка к объекту ADSI](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [протокол LDAP](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Установка сеанса LDAP](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [Привязка к объектам каталога](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>Привязка строк

Для всех функций и методов привязки требуется строка привязки. Форма строки привязки зависит от поставщика. Службы домен Active Directory поддерживаются двумя поставщиками, LDAP и WinNT.

Начиная с Windows 2000, поставщик LDAP используется для доступа к службам домен Active Directory. Строка привязки LDAP может принимать одну из следующих форм:

-   "LDAP:// <host name> / <object name> "
-   "GC:// <host name> / <object name> "

В приведенных выше примерах "LDAP:" указывает поставщика LDAP. "GC:" использует поставщик LDAP для привязки к службе глобального каталога для выполнения быстрых запросов.

" &lt; имя узла &gt; " указывает сервер для привязки и является необязательным. Если это возможно, не указывайте сервер. Также можно выполнить привязку к объекту в другом домене. Для этого передайте доменное имя целевого домена (DNS) для " &lt; имя узла &gt; ". Например, чтобы выполнить привязку к контейнеру Users в домене Домен2 объекта fabrikam.com, строка привязки будет иметь значение «LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com».

" &lt; имя объекта &gt; " представляет конкретный объект в домен Active Directory Services. Имя объекта может быть различающимся именем или идентификатором GUID объекта.

Дополнительные сведения о строках привязки LDAP см. в разделе [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).

Для Windows NT 4,0 поставщик WinNT используется для доступа к данным каталога, таким как пользователи, группы пользователей, компьютеры, службы и другие сетевые объекты в Windows 2000. Поставщик WinNT в Windows 2000 и более поздних системах имеет ограниченную функциональность по сравнению с поставщиком LDAP. Дополнительные сведения о строках привязки WinNT см. в разделе [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).

Значение ADsPath "LDAP://" или "GC://" можно использовать для привязки к корню пространства имен. При привязке к корню пространства имен указанный объект пространства имен не содержит свойств и содержит объект домена для LDAP и объект контейнера, содержащий частичную реплику всех доменов в лесу для GC.

Дополнительные сведения о привязке в домен Active Directory Services см. в следующих статьях:

-   [Бессерверная привязка и RootDSE](serverless-binding-and-rootdse.md)
-   [Привязка к глобальному каталогу](binding-to-the-global-catalog.md)
-   [Использование objectGUID для привязки к объекту](using-objectguid-to-bind-to-an-object.md)
-   [Привязка к Well-Known объектам с помощью ВКГУИД](binding-to-well-known-objects-using-wkguid.md)
-   [Привязка к объекту с помощью идентификатора безопасности](binding-to-an-object-using-a-sid.md)
-   [Включение привязки Rename-Safe с помощью свойства otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [Аутентификация](authentication.md)

 

 
