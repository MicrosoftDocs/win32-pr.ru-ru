---
title: Использование Active Directory интерфейсов служб
description: Интерфейсы служб Active Directory (ADSI) предоставляют клиентским приложениям служб каталогов возможность использовать один набор интерфейсов для взаимодействия с любым пространством имен, предоставляющим реализацию интерфейса ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Использование интерфейсов Active Directory Service Interfaces ADSI
- ADSI ADSI, использование
- Интерфейсы служб Active Directory ADSI, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15495f9fa21f436570381ea8f0b2a7c7fff5f4efed645a5f3465a3b5d2929776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648854"
---
# <a name="using-active-directory-service-interfaces"></a>Использование Active Directory интерфейсов служб

Интерфейсы служб Active Directory (ADSI) предоставляют клиентским приложениям служб каталогов возможность использовать один набор интерфейсов для взаимодействия с любым пространством имен, предоставляющим реализацию интерфейса ADSI. Для упрощения доступа к службам для пространства имен клиенты ADSI используют четко определенные интерфейсы Active Directory служб вместо вызовов API, связанных с сетью.

Active Directory интерфейсы служб соответствуют модели COM и поддерживают стандартные функции COM.

ADSI предоставляет интерфейсы, совместимые с автоматизацией для контроллеров с привязкой к имени, таких как Java, система разработки Visual Basic майкрософт и Visual Basic scripting Edition (VBScript). ADSI также предоставляет интерфейс, который может оптимизировать производительность для интерфейсов, не соответствующих автоматизации, для использования с языковыми средами, такими как C и C++.

ADSI также предоставляет интерфейсы [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) и [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), не поддерживающие автоматизацию, для поддержки управления объектами каталога и запросов.

кроме того, ADSI предоставляет собственный поставщик OLE DB, чтобы любой клиент, уже использующий OLE DB, в том числе с помощью объекты данных ActiveX, мог запрашивать службы каталогов напрямую.

Веб-приложения, использующие Active Server страницы, также могут программировать доступ к службам каталогов через ADSI.

Клиенты ADSI могут программно обнаруживать все поставщики ADSI на сайте и использовать одни и те же интерфейсы для взаимодействия с каждым пространством имен. По мере установки дополнительных поставщиков клиенты ADSI могут обмениваться данными без повторной компиляции с новыми пространствами имен.

Это руководство по программированию описывает работу ADSI и предоставляет сведения для выполнения конкретных задач в ADSI. Рассматриваются следующие темы:

-   [Привязка к объекту ADSI](binding-to-an-adsi-object.md)
-   [Создание и удаление объектов](creating-and-deleting-objects.md)
-   [Доступ к данным и управление ими с помощью ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Использование схемы ADSI](using-the-adsi-schema.md)
-   [Коллекции и группы](collections-and-groups.md)
-   [Перечисление объектов ADSI](enumerating-adsi-objects.md)
-   [Поиск Active Directory](searching-active-directory.md)
-   [Модель безопасности ADSI](adsi-security-model.md)
-   [Расширения ADSI](adsi-extensions.md)
-   [Использование ADSI с Exchange](using-adsi-with-exchange.md)
-   [Интерфейсы служебной программы ADSI](adsi-utility-interfaces.md)
-   [Программирование ADSI с помощью Java/COM](programming-adsi-with-javacom.md)

 

 




