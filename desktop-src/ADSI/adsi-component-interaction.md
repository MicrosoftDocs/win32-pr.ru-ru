---
title: Взаимодействие компонентов ADSI
description: Active Directory компонент маршрутизатора заполняет таблицу поставщика ADSI из установленных поставщиков ADSI, перечисленных в реестре при получении первого запроса от клиентского приложения.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793806"
---
# <a name="adsi-component-interaction"></a><span data-ttu-id="a0cf0-103">Взаимодействие компонентов ADSI</span><span class="sxs-lookup"><span data-stu-id="a0cf0-103">ADSI Component Interaction</span></span>

<span data-ttu-id="a0cf0-104">Active Directory компонент маршрутизатора заполняет таблицу поставщика ADSI из установленных поставщиков ADSI, перечисленных в реестре при получении первого запроса от клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="a0cf0-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="a0cf0-105">Дополнительные сведения о реестре см. [в разделе Установка компонента "пример поставщика"](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="a0cf0-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="a0cf0-106">Операции, которые делают запрос из каталога для указателя на интерфейс в Active Directoryном объекте, проходят через функцию (**GetObject** в Visual Basic или [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) в C или C++) или метод интерфейса ( [**иадсконтаинер:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span><span class="sxs-lookup"><span data-stu-id="a0cf0-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="a0cf0-107">На следующем рисунке клиентское приложение ADSI передает такой запрос на привязку компоненту маршрутизатора ADSI (1).</span><span class="sxs-lookup"><span data-stu-id="a0cf0-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="a0cf0-108">Компонент маршрутизатора определяет ProgID для поставщика из первой части ADsPath и использует [**клсидфромпрогид**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) для поиска соответствующего идентификатора CLSID в реестре (2) и загружает соответствующий компонент поставщика (3).</span><span class="sxs-lookup"><span data-stu-id="a0cf0-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![взаимодействие компонентов ADSI в примере поставщика](images/dscspr.png)

<span data-ttu-id="a0cf0-110">На предыдущем рисунке компонент поставщика создает объект Active Directory, представляющий элемент именованного каталога.</span><span class="sxs-lookup"><span data-stu-id="a0cf0-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="a0cf0-111">Компонент поддержки ADSI выполняет **QueryInterface** на запрошенном идентификаторе интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a0cf0-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="a0cf0-112">При получении указателя на этот интерфейс (4), как и для всех реализаций клиента и сервера COM, он передается обратно клиенту (5), а затем в клиентском приложении работает непосредственно с компонентом поставщика (6).</span><span class="sxs-lookup"><span data-stu-id="a0cf0-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 