---
title: Чтение набора прав доступа к элементу управления в ACL объекта
description: Свойства интерфейса Иадсакцессконтролентри используются для предоставления или запрета прав на управление доступом.
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- Чтение набора прав доступа к элементу управления, заданного в списке ACL объекта Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877c96a95fc94095c79ad129e8a07b1c786abe1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069755"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>Чтение набора прав доступа к элементу управления в ACL объекта

С помощью ADSI вы читаете элемент управления ACE Right, как и любой другой элемент ACE в списке ACL. Имейте в виду, что для чтения списков управления доступом к объектам каталога можно также использовать API-интерфейсы безопасности Win32. Однако права доступа управления используют свойства интерфейса [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) так, как это характерно для предоставления и запрета прав на доступ к управлению:

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) должен содержать **рекламу \_ с \_ правом \_ \_ доступа к DS**.
-   Значение [**флагов**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) имеет **\_ \_ тип объекта \_ \_ флага ADS**.
-   [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) — это строковый формат атрибута **ригхтсгуид** права доступа к элементу управления. Строковый формат GUID имеет тот же формат строки, что и функция библиотеки COM [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) .
-   [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) — это **рекламное объявление \_ AceType \_ Access \_ Allowed \_ Object** , чтобы предоставить доверенному лицу доступ к элементу управления право доступа или **ADS \_ AceType \_ доступ \_ запрещен \_** , чтобы запретить доверенному лицу право доступа к элементу управления.
-   [**Доверенное лицо**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) — это субъект безопасности; Это пользователь, группа, компьютер и т. д., к которым применяется ACE.

Используйте следующую процедуру, чтобы прочитать ACE для объекта ADSI. Следующая процедура применима к приложениям C и C++.

**Чтение ACE для объекта ADSI**

1.  Получите указатель интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) для объекта.
2.  Чтобы получить дескриптор безопасности объекта, используйте метод [**iAds:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) . Имя свойства, содержащего дескриптор безопасности, — "Нтсекуритидескриптор". Свойство будет возвращено как **значение типа Variant** , содержащее указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Имейте в виду, что элемент **VT** является компонентом **VT \_ Dispatch**. Вызовите **QueryInterface** на этом указателе **IDispatch** , чтобы получить интерфейс [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) , чтобы использовать методы этого интерфейса для доступа к ACL дескриптора безопасности.
3.  Используйте метод [**иадссекуритидескриптор:: Get \_ дискретионарякл**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) для получения списка ACL. Метод возвращает указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Вызовите метод **QueryInterface** для этого указателя **IDispatch** , чтобы получить интерфейс [**иадсакцессконтроллист**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) , чтобы использовать методы этого интерфейса для доступа к отдельным записям ACE в списке управления доступом.
4.  Используйте метод [**иадсакцессконтроллист:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) для перечисления записей ACE. Метод возвращает указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Вызовите **QueryInterface** на этом указателе **IUnknown** , чтобы получить интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .
5.  Используйте метод [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) для перечисления записей ACE в списке ACL. Свойство возвращается как **значение типа Variant** , содержащее указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Имейте в виду, что элемент **VT** является компонентом **VT \_ Dispatch**. Вызовите метод **QueryInterface** для этого указателя **IDispatch** , чтобы получить интерфейс [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) для чтения элемента управления доступом.
6.  Вызовите [**метод иадсакцессконтролентри:: \_ Get AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) для получения значения **AccessMask** и убедитесь, что значение **AccessMask** для флага **\_ \_ \_ \_ доступа к AD DS right** . Если у него есть этот флаг, ACE содержит право доступа к элементу управления.
7.  Вызовите метод [**иадсакцессконтролентри:: Get \_ flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) , чтобы получить флаг для типа объекта.
8.  Флаг [**проверки значения флагов**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) для **\_ типа объекта флага объявлений \_ \_ \_ Present** . Если для **флагов** задано значение **\_ \_ \_ тип объекта \_ флага ADS**, вызовите метод **иадсакцессконтролентри:: Get \_ ObjectType** , чтобы получить строку, содержащую ригхтсгуид элемента управления, к которому применяется ACE.
9.  Вызовите метод [**иадсакцессконтролентри:: Get \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) , чтобы получить тип ACE. Тип будет представлять собой **баннер \_ ACETYPE \_ Access \_ Allowed \_ Object** , чтобы предоставить доверенному лицу доступ к объекту Control право доступа или **AD \_ ACETYPE \_ \_ Denied \_** для запрета права доступа к элементу управления.
10. Вызовите метод [**иадсакцессконтролентри:: Get \_ для**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) получения субъекта безопасности, который является пользователем, группой, компьютером и т. д., к которому применяется ACE.
11. После завершения работы с строками [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) и **доверенного лица** используйте [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) , чтобы освободить память для этих строк.
12. После завершения работы с интерфейсами вызовите метод **Release** , чтобы уменьшить или освободить все ссылки на интерфейс.

 

 