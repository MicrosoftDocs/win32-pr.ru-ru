---
description: Предоставляет сведения об учетных данных, относящиеся к SChannel.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Запрос атрибутов учетных данных SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264360"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="36d6e-103">Запрос атрибутов учетных данных SChannel</span><span class="sxs-lookup"><span data-stu-id="36d6e-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="36d6e-104">Функция [**куерикредентиалсаттрибутес**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) предоставляет сведения об учетных данных, относящиеся к SChannel.</span><span class="sxs-lookup"><span data-stu-id="36d6e-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="36d6e-105">Эти сведения первоначально указываются при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="36d6e-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="36d6e-106">Дополнительные сведения см. в разделе [Получение учетных данных SChannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="36d6e-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="36d6e-107">Сведения, сообщаемые этой функцией, допустимы для любых подключений ([*контекстов безопасности*](../secgloss/s-gly.md)), созданных с помощью указанных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="36d6e-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
