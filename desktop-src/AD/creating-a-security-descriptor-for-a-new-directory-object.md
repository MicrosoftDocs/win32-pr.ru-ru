---
title: Создание дескрипторов безопасности для новых объектов каталога
description: С помощью ADSI можно создать дескриптор безопасности и задать его в качестве свойства Нтсекуритидескриптор нового объекта или использовать его для замены свойства Нтсекуритидескриптор существующего объекта.
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- Создание дескриптора безопасности для нового объекта каталога Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487476"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>Создание дескрипторов безопасности для новых объектов каталога

С помощью ADSI можно создать дескриптор безопасности и задать его в качестве свойства **нтсекуритидескриптор** нового объекта или использовать его для замены свойства **нтсекуритидескриптор** существующего объекта.

Чтобы создать дескриптор безопасности для объекта, выполните следующие действия.

1.  Используйте [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания com-объекта ADSI для нового дескриптора безопасности и получения указателя интерфейса [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) на этот объект. Имейте в виду, что ИДЕНТИФИКАТОРом класса является **CLSID \_ SecurityDescriptor**.
2.  Используйте метод [**иадссекуритидескриптор::p UT \_ owner**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) , чтобы задать владельца объекта. Доверенное лицо — это пользователь, группа или другой субъект безопасности. Приложение должно использовать значение из соответствующего свойства из объекта пользователя или группы доверенного лица, к которому применяется ACE.
3.  Используйте метод [**\_ управления иадссекуритидескриптор::p UT**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) для управления наследованием DACL и SACL объектом из родительского контейнера.
4.  Используйте [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания com-объекта ADSI для списка DACL для нового дескриптора безопасности и получения указателя интерфейса [**иадсакцессконтроллист**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) на этот объект. Имейте в виду, что ИДЕНТИФИКАТОРом класса является **CLSID \_ акцессконтроллист**.
5.  Для каждого элемента ACE, добавляемого в список DACL, используйте [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания com-объекта ADSI для нового элемента ACE и получения указателя интерфейса [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) на этот объект. Имейте в виду, что ИДЕНТИФИКАТОРом класса является CLSID \_ акцессконтролентри.
6.  Для каждого элемента ACE, добавляемого в список DACL, задайте свойства элемента управления доступом с помощью методов свойств объекта [**ИАДСАКЦЕССКОНТРОЛЕНТРИ**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) ACE. Дополнительные сведения о свойствах, которые необходимо задать для записи ACE, см. [в разделе Установка прав доступа для объекта](setting-access-rights-on-an-object.md).
7.  Для каждого элемента ACE, добавляемого в список DACL, используйте метод **QueryInterface** объекта [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) для получения указателя [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Для метода [**иадсакцессконтроллист:: аддаце**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) требуется указатель интерфейса **IDispatch** на элемент управления доступом.
8.  Для каждого элемента ACE, добавляемого в список DACL, используйте [**иадсакцессконтроллист:: аддаце**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) , чтобы добавить новый элемент управления доступом в список DACL. Имейте в виду, что порядок элементов ACE в списке ACL может повлиять на оценку доступа к объекту. Для правильного доступа к объекту может потребоваться создать новый список ACL, добавить записи ACE из существующего списка ACL в правильном порядке в новый список управления доступом, а затем заменить существующий список ACL в дескрипторе безопасности новым ACL. Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).
9.  Выполните шаги 4-8, чтобы создать список SACL для нового дескриптора безопасности.
10. Чтобы задать список DACL, используйте метод [**иадссекуритидескриптор::p UT \_ дискретионарякл**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) . Дополнительные сведения о списках DACL см. в разделе пустые [списки DACL и пустой список DACL](null-dacls-and-empty-dacls.md).
11. Чтобы задать список SACL, используйте метод [**иадссекуритидескриптор::p UT \_ системакл**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) .
12. Преобразуйте объект [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) в [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) с помощью метода **QueryInterface** объекта **иадссекуритидескриптор** , чтобы получить интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Затем **установите для элемента** **VT** в качестве значения **VT \_ Dispatch** и задайте для элемента **пдиспвал** объекта **Variant** значение, равное указателю **IDispatch** .
13. Получите указатель интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) для объекта.
14. Используйте метод [**iAds::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) с параметром "нтсекуритидескриптор" и [**вариантом**](/windows/win32/api/oaidl/ns-oaidl-variant) , созданным выше, чтобы записать новый дескриптор безопасности в кэш свойств.
15. Используйте метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) , чтобы обновить свойство объекта в каталоге.

 

 