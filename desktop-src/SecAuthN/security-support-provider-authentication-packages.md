---
description: Операционная система Windows поддерживает проверку подлинности с помощью пакетов безопасности, которые работают как в качестве поставщиков поддержки безопасности, так и в качестве пакетов проверки подлинности.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Поставщик поддержки безопасности/пакеты проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647345"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="ee683-103">Поставщик поддержки безопасности/пакеты проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="ee683-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="ee683-104">Операционная система Windows поддерживает проверку подлинности с помощью [*пакетов безопасности*](../secgloss/s-gly.md) , которые работают как в качестве [*поставщиков поддержки безопасности*](../secgloss/s-gly.md) , так и в качестве [*пакетов проверки подлинности*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ee683-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="ee683-105">Пакеты безопасности предоставляют службы поддержки процесса входа в систему пакета проверки подлинности Windows, а также предоставляют службы проверки подлинности приложениям путем реализации набора функций, сопоставленных с [интерфейсом поставщика поддержки безопасности](sspi.md) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="ee683-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="ee683-106">Пакет безопасности, который работает как пакет проверки подлинности и реализует функциональные возможности, необходимые для [*SSPI*](../secgloss/s-gly.md) , называется поставщиком поддержки безопасности/пакетом проверки подлинности (SSP или AP).</span><span class="sxs-lookup"><span data-stu-id="ee683-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="ee683-107">Дополнительные сведения о пакетах безопасности см. [в разделе пакеты SSP, предоставляемые корпорацией Майкрософт](ssp-packages-provided-by-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="ee683-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="ee683-108">Сведения о разработке пользовательских поставщиков общих служб и ТД см. в разделе [пользовательские пакеты безопасности](custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="ee683-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
