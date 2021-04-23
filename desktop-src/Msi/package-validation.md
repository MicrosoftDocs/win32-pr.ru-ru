---
description: Настоятельно рекомендуется выполнять проверку для каждого нового или только что измененного пакета установки, прежде чем пытаться установить пакет в первый раз.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Проверка пакета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898849"
---
# <a name="package-validation"></a><span data-ttu-id="1d205-103">Проверка пакета</span><span class="sxs-lookup"><span data-stu-id="1d205-103">Package Validation</span></span>

<span data-ttu-id="1d205-104">Настоятельно рекомендуется выполнять проверку для каждого нового или только что измененного пакета установки, прежде чем пытаться установить пакет в первый раз.</span><span class="sxs-lookup"><span data-stu-id="1d205-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="1d205-105">Проверка пакета включает в себя следующие три процесса:</span><span class="sxs-lookup"><span data-stu-id="1d205-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="1d205-106">Внутренняя проверка</span><span class="sxs-lookup"><span data-stu-id="1d205-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="1d205-107">Проверка пула строк</span><span class="sxs-lookup"><span data-stu-id="1d205-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="1d205-108">Внутренние средства оценки согласованности — ICEs</span><span class="sxs-lookup"><span data-stu-id="1d205-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="1d205-109">Модули слияния следует проверять с помощью метода, описанного в разделе [Проверка модулей слияния](validating-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="1d205-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="1d205-110">Evalcom2.dll предоставляет COM-объект, который реализует операции проверки для пакетов установки и модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="1d205-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="1d205-111">Основной объект реализует интерфейсы для программ C/C++.</span><span class="sxs-lookup"><span data-stu-id="1d205-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="1d205-112">Дополнительные сведения см. в разделе [Автоматизация проверки](validation-automation.md).</span><span class="sxs-lookup"><span data-stu-id="1d205-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 



