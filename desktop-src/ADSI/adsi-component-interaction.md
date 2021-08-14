---
title: Взаимодействие компонентов ADSI
description: Active Directory компонент маршрутизатора заполняет таблицу поставщика ADSI из установленных поставщиков ADSI, перечисленных в реестре при получении первого запроса от клиентского приложения.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec82573c23564c964ebe310cd7eceb917a4565ed2d6fa8aa40b4dc03d1db2d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181116"
---
# <a name="adsi-component-interaction"></a>Взаимодействие компонентов ADSI

Active Directory компонент маршрутизатора заполняет таблицу поставщика ADSI из установленных поставщиков ADSI, перечисленных в реестре при получении первого запроса от клиентского приложения. Дополнительные сведения о реестре см. [в разделе Установка компонента "пример поставщика"](installing-the-example-provider-component.md).

операции, которые делают запрос из каталога для указателя на интерфейс в Active Directoryном объекте, проходят через функцию (**getobject** в Visual Basic или [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) в C или C++) или метод интерфейса ( [**иадсконтаинер:: getobject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). На следующем рисунке клиентское приложение ADSI передает такой запрос на привязку компоненту маршрутизатора ADSI (1). Компонент маршрутизатора определяет ProgID для поставщика из первой части ADsPath и использует [**клсидфромпрогид**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) для поиска соответствующего идентификатора CLSID в реестре (2) и загружает соответствующий компонент поставщика (3).

![взаимодействие компонентов ADSI в примере поставщика](images/dscspr.png)

На предыдущем рисунке компонент поставщика создает объект Active Directory, представляющий элемент именованного каталога. Компонент поддержки ADSI выполняет **QueryInterface** на запрошенном идентификаторе интерфейса. При получении указателя на этот интерфейс (4), как и для всех реализаций клиента и сервера COM, он передается обратно клиенту (5), а затем в клиентском приложении работает непосредственно с компонентом поставщика (6).

 

 