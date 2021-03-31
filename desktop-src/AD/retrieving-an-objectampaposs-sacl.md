---
title: Получение списка SACL объекта
description: Дескриптор безопасности объекта в домен Active Directory Services может содержать системный список управления доступом (SACL).
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- СПИСОК SACL ACTIVE DIRECTORY
- SACL Active Directory, Извлечение списка SACL объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537846f2080aecdab8e22f5fce5bdfa36298fb74
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336777"
---
# <a name="retrieving-an-objects-sacl"></a>Получение списка SACL объекта

Дескриптор безопасности объекта в домен Active Directory Services может содержать системный список управления доступом (SACL). Список SACL содержит записи управления доступом (ACE), которые указывают типы попыток доступа, которые создают записи аудита в журнале событий безопасности контроллера домена. Имейте в виду, что список SACL создает записи журнала только на контроллере домена, где произошла попыток доступа, а не на каждом контроллере домена, содержащем реплику объекта.

Чтобы задать или получить список SACL из дескриптора безопасности объекта, необходимо включить разрешение **\_ \_ имени безопасности SE** в маркере доступа запрашивающего потока. Группа Администраторы по умолчанию имеет эту привилегию и может быть назначена другим пользователям или группам. Дополнительные сведения см. в статье [право доступа к SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Чтобы получить и задать список SACL для объекта каталога, используйте интерфейс [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . С помощью C++ метод [**иадссекуритидескриптор:: Get \_ системакл**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) возвращает указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Вызовите метод **QueryInterface** для этого указателя **IDispatch** , чтобы получить интерфейс [**иадсакцессконтроллист**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) , и используйте методы этого интерфейса для доступа к отдельным записям ACE в списке SACL. Дополнительные сведения о процедуре изменения списка SACL, подобной изменению списка DACL, см. в разделе [Установка прав доступа для объекта](setting-access-rights-on-an-object.md).

Чтобы перечислить ACE в списке SACL, используйте метод [**иадсакцессконтроллист:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) , который возвращает указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Вызовите **QueryInterface** на этом указателе **IUnknown** , чтобы получить интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Используйте метод [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) для перечисления записей ACE в списке ACL. Каждый элемент ACE возвращается как **вариант** , содержащий указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ; Имейте в виду, что элемент **VT** является компонентом **VT \_ Dispatch**. Вызовите метод **QueryInterface** для этого указателя **IDispatch** , чтобы получить интерфейс [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) для элемента управления доступом. Используйте методы интерфейса **иадсакцессконтролентри** , чтобы задать или получить компоненты ACE.

Дополнительные сведения о SACL см. в следующих статьях:

-   [Списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Создание записей аудита](/windows/desktop/SecAuthZ/audit-generation)

 

 