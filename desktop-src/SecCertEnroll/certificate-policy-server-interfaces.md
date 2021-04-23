---
description: Для программной настройки сервера политики регистрации сертификатов (CEP) можно использовать следующие интерфейсы.
ms.assetid: 48c7c21c-1b20-4a79-932d-bed19ff9833e
title: Интерфейсы сервера политики сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c16373c2bac364a91af2cdadf6a8d33445e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543535"
---
# <a name="certificate-policy-server-interfaces"></a><span data-ttu-id="8a526-103">Интерфейсы сервера политики сертификатов</span><span class="sxs-lookup"><span data-stu-id="8a526-103">Certificate Policy Server Interfaces</span></span>

<span data-ttu-id="8a526-104">Для программной настройки сервера политики регистрации сертификатов (CEP) можно использовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8a526-104">The following interfaces can be used to programmatically configure a certificate enrollment policy (CEP) server.</span></span>



| <span data-ttu-id="8a526-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8a526-105">Interface</span></span>                                                            | <span data-ttu-id="8a526-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8a526-106">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a526-107">**IX509EnrollmentPolicyServer**</span><span class="sxs-lookup"><span data-stu-id="8a526-107">**IX509EnrollmentPolicyServer**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmentpolicyserver)   | <span data-ttu-id="8a526-108">Представляет сервер обработки сложных событий.</span><span class="sxs-lookup"><span data-stu-id="8a526-108">Represents a CEP server.</span></span>                                                                                      |
| [<span data-ttu-id="8a526-109">**IX509PolicyServerListManager**</span><span class="sxs-lookup"><span data-stu-id="8a526-109">**IX509PolicyServerListManager**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509policyserverlistmanager) | <span data-ttu-id="8a526-110">Управляет коллекцией объектов [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl) .</span><span class="sxs-lookup"><span data-stu-id="8a526-110">Manages a collection of [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl) objects.</span></span>                         |
| [<span data-ttu-id="8a526-111">**IX509PolicyServerUrl**</span><span class="sxs-lookup"><span data-stu-id="8a526-111">**IX509PolicyServerUrl**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl)                 | <span data-ttu-id="8a526-112">Указывает или получает значения свойств, связанные с сервером обработки сложных событий, и обновляет связанные значения реестра.</span><span class="sxs-lookup"><span data-stu-id="8a526-112">Specifies or retrieves property values associated with the CEP server and updates associated registry values.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8a526-113">См. также</span><span class="sxs-lookup"><span data-stu-id="8a526-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a526-114">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="8a526-114">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



