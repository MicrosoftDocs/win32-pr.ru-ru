---
title: Получение списка DACL объекта
description: Дескриптор безопасности объекта может содержать список управления доступом на уровне пользователей (DACL).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL ACTIVE DIRECTORY
- DACL Active Directory, получение списка DACL объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025112"
---
# <a name="retrieving-an-objects-dacl"></a>Получение списка DACL объекта

Дескриптор безопасности объекта может содержать список управления доступом на уровне пользователей (DACL). Список DACL содержит ноль или больше записей управления доступом (ACE), которые определяют пользователей и группы, которым разрешен доступ к объекту. Если список DACL пуст (т. е. он содержит ноль ACE), доступ явно не предоставляется, поэтому доступ неявно запрещается. Однако если у дескриптора безопасности объекта нет DACL, объект не защищен и все пользователи имеют полный доступ.

Чтобы получить список DACL объекта, необходимо быть владельцем объекта или иметь доступ на **Чтение \_** к объекту.

Чтобы получить и задать список DACL для объекта каталога, используйте интерфейс [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . С помощью C++ метод [**иадссекуритидескриптор:: Get \_ дискретионарякл**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) возвращает указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Вызовите метод **QueryInterface** для этого указателя **IDispatch** , чтобы получить интерфейс [**иадсакцессконтроллист**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) , и используйте методы этого интерфейса для доступа к отдельным записям ACE в списке DACL. Процедура изменения списка DACL описана в разделе [Установка прав доступа для объекта](setting-access-rights-on-an-object.md).

Чтобы перечислить ACE, используйте метод [**иадсакцессконтроллист:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) . Метод возвращает указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Вызовите **QueryInterface** на этом указателе **IUnknown** , чтобы получить интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Используйте метод [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) для перечисления записей ACE в списке ACL. Каждый элемент ACE возвращается в виде **варианта** , содержащего указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (элемент **VT** — это **\_ диспетчеризация**). Вызовите метод **QueryInterface** для этого указателя **IDispatch** , чтобы получить интерфейс [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) для элемента управления доступом. Для установки или получения компонентов ACE можно использовать методы интерфейса **иадсакцессконтролентри** .

Дополнительные сведения об DACL и ACE см. в следующих разделах, посвященных набору средств разработки программного обеспечения (SDK) платформы.

-   [Списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Записи управления доступом (ACE)](/windows/desktop/SecAuthZ/access-control-entries)

 

 