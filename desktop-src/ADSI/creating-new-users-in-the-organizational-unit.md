---
title: Создание новых пользователей в подразделении
description: Терри Адамс был принят на работу в компании Fabrikam Sales. Его прямой отчет — Патрик Хинес.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Создание новых пользователей в подразделении ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486565"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>Создание новых пользователей в подразделении

Терри Адамс был принят на работу в компании Fabrikam Sales. Его прямой отчет — Патрик Хинес.

Как показано в следующем примере кода, Джо Новиков, администратор предприятия, создаст для него новую учетную запись.


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



При создании нового пользователя необходимо указать **SamAccountName**. Это обязательный атрибут для класса User. Прежде чем можно будет создать экземпляр объекта, необходимо задать все обязательные атрибуты. **SamAccountName** будет автоматически сформирован, если он не указан для нового пользователя.

При создании нового пользователя все необходимые атрибуты должны быть установлены в локальном кэше перед вызовом метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

Джо, как администратор, может назначить пароль Терри с помощью метода [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) . Метод **IADsUser. SetPassword** не будет работать до вызова метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

Затем Сергей включает учетную запись пользователя, присвоив свойству [**IADsUser. Аккаунтдисаблед**](iadsuser-property-methods.md) **значение false**.

В следующем примере кода показано, как задать Терри в качестве менеджера Патрик.


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



Может возникнуть вопрос, что произойдет, если Терри изменит свое имя, перейдет в другую организацию или покидает компанию. Кто обслуживает связь «руководитель — прямой отчет»? Дополнительные сведения и решение этой проблемы см. в разделе [reorganization](reorganization.md). Поскольку схема Active Directory является расширяемой, вы можете моделировать объекты для включения аналогичных связей между руководителями и подчиненными стилями.

Прежде чем перейти к следующей задаче, Взгляните на пример кода, демонстрирующий, как Сергей будет просматривать непосредственные подчиненные отчеты Терри.


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



В этом примере кода Патрик будет отображаться как прямой отчет Терри, даже если атрибут **directReports** никогда не изменялся. Active Directory выполняет это автоматически.

В мире каталога атрибут может иметь одно или несколько значений. Поскольку **directReports** имеет несколько значений, эти сведения можно получить, просмотрев схему, проще использовать метод [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) , который возвращает массив значений независимо от того, возвращено ли одно или несколько значений.

Оснастка Active Directory пользователи и компьютеры позволяет просматривать непосредственные связи между отчетами и менеджерами на странице свойств пользователя.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Добавление пользователей в группу](adding-users-to-a-group.md)
</dt> </dl>

 

 




