---
title: Необязательная реализация
description: Следующие функции являются необязательными, но рекомендуется
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Необязательная реализация ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531841"
---
# <a name="optional-implementation"></a><span data-ttu-id="fb1ba-104">Необязательная реализация</span><span class="sxs-lookup"><span data-stu-id="fb1ba-104">Optional Implementation</span></span>

<span data-ttu-id="fb1ba-105">Следующие функции являются необязательными, но рекомендуется:</span><span class="sxs-lookup"><span data-stu-id="fb1ba-105">The following features are optional, but recommended:</span></span>

-   <span data-ttu-id="fb1ba-106">Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) для клиентов, не поддерживающих автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for non-Automation clients.</span></span> <span data-ttu-id="fb1ba-107">Так как поставщик OLE DB ADSI использует **IDirectorySearch** для представления запросов и получения результатов из базовой службы каталогов, поставщики, реализующие этот интерфейс, автоматически предоставляют доступ к базам данных OLE DB стилей, не прибегая к реализации каких-либо дополнительных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-107">Because the ADSI OLE DB provider uses **IDirectorySearch** to present queries and collect results from the underlying directory service, providers that implement this interface automatically provide access to OLE DB style databases without having to implement any additional interfaces.</span></span>
-   <span data-ttu-id="fb1ba-108">Интерфейсы [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)и [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="fb1ba-108">The [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interfaces.</span></span> <span data-ttu-id="fb1ba-109">Поставщики служб каталогов, поддерживающие безопасность объектов на основе списков управления доступом, рекомендуется применять к этим дополнительным функциям.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-109">Providers for directory services that support ACL-based object security are encouraged to implement these additional features.</span></span>

 

 




