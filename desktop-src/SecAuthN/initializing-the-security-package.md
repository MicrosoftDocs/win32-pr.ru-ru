---
description: Содержит список и описание действий, необходимых для инициализации пакета безопасности.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Инициализация пакета безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156027"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="0e74d-103">Инициализация пакета безопасности</span><span class="sxs-lookup"><span data-stu-id="0e74d-103">Initializing the Security Package</span></span>

<span data-ttu-id="0e74d-104">Перед использованием SSPI необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e74d-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="0e74d-105">Для получения адреса таблицы функции безопасности необходимо вызвать функцию инициализации.</span><span class="sxs-lookup"><span data-stu-id="0e74d-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="0e74d-106">Клиент и сервер вызывают [**инитсекуритинтерфаце**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) для указателя на таблицу диспетчеризации [**секуритифунктионтабле**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) .</span><span class="sxs-lookup"><span data-stu-id="0e74d-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="0e74d-107">Эта таблица содержит указатели на функции обратного вызова, объявленные в SSPI. h.</span><span class="sxs-lookup"><span data-stu-id="0e74d-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="0e74d-108">Эти указатели предоставляют доступ к реализациям библиотек DLL различных функций SSPI.</span><span class="sxs-lookup"><span data-stu-id="0e74d-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="0e74d-109">Необходимо получить сведения о поддерживаемых пакетах безопасности.</span><span class="sxs-lookup"><span data-stu-id="0e74d-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="0e74d-110">Хотя большинство приложений используют пакеты безопасности, поддерживающие стандартные или стандартные возможности, пакеты безопасности могут иметь уникальные возможности для приложения.</span><span class="sxs-lookup"><span data-stu-id="0e74d-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="0e74d-111">Приложение, требующее специальных возможностей, может использовать пакет, предлагающий эти возможности.</span><span class="sxs-lookup"><span data-stu-id="0e74d-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="0e74d-112">Дополнительные сведения см. в разделе [Получение сведений о пакетах безопасности](getting-information-about-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0e74d-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="0e74d-113">На этом этапе приложение успешно инициализировал SSP и выбрал пакет безопасности с достаточными возможностями.</span><span class="sxs-lookup"><span data-stu-id="0e74d-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="0e74d-114">Пакет [*Negotiate*](../secgloss/n-gly.md) можно использовать там, где соглашение между клиентом и сервером, какой [*пакет безопасности*](../secgloss/s-gly.md) следует использовать, выполняется в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="0e74d-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="0e74d-115">Если пакет Negotiate не используется, клиент и сервер должны согласиться с использованием конкретного пакета безопасности перед выполнением описанных выше шагов установки.</span><span class="sxs-lookup"><span data-stu-id="0e74d-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
