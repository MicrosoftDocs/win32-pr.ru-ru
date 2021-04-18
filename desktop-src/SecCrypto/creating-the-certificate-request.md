---
description: Процесс создания запроса на сертификат включает сбор определенных сведений от инициатора запроса.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Создание запроса на сертификат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662326"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="c5c70-103">Создание запроса на сертификат</span><span class="sxs-lookup"><span data-stu-id="c5c70-103">Creating the Certificate Request</span></span>

<span data-ttu-id="c5c70-104">Процесс создания запроса на сертификат включает сбор определенных сведений от инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="c5c70-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="c5c70-105">Обычно это делается с помощью какого-либо пользовательского интерфейса, хотя данные могут быть взяты непосредственно из базы данных без необходимости в ПОЛЬЗОВАТЕЛЬСКОМ интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c5c70-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="c5c70-106">Требуемый уровень информации задается политикой [*центра сертификации*](../secgloss/c-gly.md) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="c5c70-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="c5c70-107">Пример необходимой информации может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="c5c70-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="c5c70-108">Общее имя</span><span class="sxs-lookup"><span data-stu-id="c5c70-108">Common Name</span></span>
-   <span data-ttu-id="c5c70-109">Имя единицы измерения</span><span class="sxs-lookup"><span data-stu-id="c5c70-109">Unit Name</span></span>
-   <span data-ttu-id="c5c70-110">Название организации</span><span class="sxs-lookup"><span data-stu-id="c5c70-110">Company Name</span></span>
-   <span data-ttu-id="c5c70-111">Город</span><span class="sxs-lookup"><span data-stu-id="c5c70-111">City</span></span>
-   <span data-ttu-id="c5c70-112">Состояние</span><span class="sxs-lookup"><span data-stu-id="c5c70-112">State</span></span>
-   <span data-ttu-id="c5c70-113">Страна или регион</span><span class="sxs-lookup"><span data-stu-id="c5c70-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="c5c70-114">Интерфейс предназначен для создания одного запроса для каждого экземпляра xenroll.</span><span class="sxs-lookup"><span data-stu-id="c5c70-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="c5c70-115">Для создания каждого [*запроса на сертификат*](../secgloss/c-gly.md)необходимо создать отдельный экземпляр xenroll.</span><span class="sxs-lookup"><span data-stu-id="c5c70-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="c5c70-116">Сведения о том, как использовать Управление регистрацией сертификатов для запроса сертификата на конкретных языках программирования, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c5c70-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="c5c70-117">Пример запроса в C++</span><span class="sxs-lookup"><span data-stu-id="c5c70-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="c5c70-118">Запрос примера в VBScript</span><span class="sxs-lookup"><span data-stu-id="c5c70-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
