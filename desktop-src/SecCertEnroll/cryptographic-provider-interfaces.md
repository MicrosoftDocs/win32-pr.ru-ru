---
description: Для получения сведений о поставщиках служб шифрования можно использовать следующие интерфейсы.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Интерфейсы поставщика служб шифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154734"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="387aa-103">Интерфейсы поставщика служб шифрования</span><span class="sxs-lookup"><span data-stu-id="387aa-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="387aa-104">Для получения сведений о поставщиках служб шифрования можно использовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="387aa-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="387aa-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="387aa-105">Interface</span></span>                                    | <span data-ttu-id="387aa-106">Описание</span><span class="sxs-lookup"><span data-stu-id="387aa-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="387aa-107">**икспалгорисм**</span><span class="sxs-lookup"><span data-stu-id="387aa-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="387aa-108">Представляет алгоритм, реализованный поставщиком служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="387aa-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="387aa-109">**икспалгорисмс**</span><span class="sxs-lookup"><span data-stu-id="387aa-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="387aa-110">Управляет коллекцией объектов [**икспалгорисм**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="387aa-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="387aa-111">**икспинформатион**</span><span class="sxs-lookup"><span data-stu-id="387aa-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="387aa-112">Предоставляет доступ к общим сведениям о поставщике служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="387aa-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="387aa-113">**икспинформатионс**</span><span class="sxs-lookup"><span data-stu-id="387aa-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="387aa-114">Управляет коллекцией объектов [**икспинформатион**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .</span><span class="sxs-lookup"><span data-stu-id="387aa-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="387aa-115">**икспстатус**</span><span class="sxs-lookup"><span data-stu-id="387aa-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="387aa-116">Содержит сведения о паре поставщика или алгоритма шифрования.</span><span class="sxs-lookup"><span data-stu-id="387aa-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="387aa-117">**икспстатусес**</span><span class="sxs-lookup"><span data-stu-id="387aa-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="387aa-118">Управляет коллекцией объектов [**икспстатус**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .</span><span class="sxs-lookup"><span data-stu-id="387aa-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="387aa-119">См. также</span><span class="sxs-lookup"><span data-stu-id="387aa-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="387aa-120">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="387aa-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



