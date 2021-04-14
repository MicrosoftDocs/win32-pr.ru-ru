---
description: Когда WUA обнаруживает, что вызывающий объект не имеет разрешения на доступ к интерфейсу, методу или свойству, возвращается значение HRESULT E \_ ACCESSDENIED.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Защита интерфейсов, методов и свойств в API-интерфейсе WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692472"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Защита интерфейсов, методов и свойств в API-интерфейсе WUA

Некоторые интерфейсы, методы и свойства агента Центр обновления Windows (WUA) доступны только вызывающим объектам, принадлежащим следующим группам безопасности Windows:

-   Администратор
-   Пользователь
-   Опытный пользователь

Когда WUA обнаруживает, что вызывающий объект не имеет разрешения на доступ к интерфейсу, методу или свойству, возвращается значение **HRESULT** E \_ ACCESSDENIED.

Для групп безопасности администратора, пользователя и опытного пользователя доступны следующие интерфейсы:

-   [**иаутоматикупдатес**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**исистеминформатион**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**иупдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**Иупдатесессион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) и [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Если выполняются следующие условия, поиск завершается ошибкой:
>
> -   Пользователь, не являющийся администратором, задает для [**Свойства UserLocale интерфейса IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) языковой стандарт, соответствующий языку, который не установлен на компьютере.
> -   Поиск использует объект Упдатесеарч, созданный из объекта UpdateSession.

 

Следующие интерфейсы и методы загрузки доступны для групп "Администраторы" и "Опытные пользователи":

-   [**иупдатедовнлоадер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**Иупдате:: Копифромкаче**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2:: Чеккпермиссион**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Администраторы, пользователи и опытные пользователи могут вызывать [**IAutomaticUpdatesSettings2:: чеккпермиссион**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).

     

Следующие интерфейсы, методы и свойства установки доступны для групп администраторов:

-   [**Иаутоматикупдатес::P Аусе**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**Иаутоматикупдатес:: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**Иаутоматикупдатес:: Енаблесервице**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**иупдатеинсталлер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**Свойство Hidden объекта Иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Администраторы, пользователи и опытные пользователи могут извлекать значения [**свойства Hidden объекта иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden). Тем не менее, значения могут быть заданы только администраторам и опытным пользователям.

     

-   [**Иупдате:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Администраторы и опытные пользователи могут вызывать [**метод AcceptEula иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).

     

-   [**Иаутоматикупдатессеттингс:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**Свойство Нотификатионлевел объекта Иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства нотификатионлевел объекта иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel). Однако значения могут быть заданы только администраторами.

     

-   [**Свойство Счедулединсталлатиондай объекта Иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства счедулединсталлатиондай объекта иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday). Однако значения могут быть заданы только администраторами.

     

-   [**Свойство Счедулединсталлатионтиме объекта Иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства счедулединсталлатионтиме объекта иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Однако значения могут быть заданы только администраторами.

     

-   [**Свойство Инклудерекоммендедупдатес объекта IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства инклудерекоммендедупдатес объекта IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates). Однако значения могут быть заданы только администраторами.

     

 

 



