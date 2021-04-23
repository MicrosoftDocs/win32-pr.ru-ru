---
title: Примеры приложений на C++ BITS
description: Примеры приложений фоновая интеллектуальная служба передачи (BITS) в этом разделе написаны на C++. Они демонстрируют ряд задач, которые можно выполнить с помощью функций службы BITS. Каждое приложение разделено на несколько шагов.
ms.assetid: 6163c7fd-e187-4f75-bf25-e3a515e50db5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf577509dac58a655c2cbc8b602b75bd48aa03e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070373"
---
# <a name="bits-c-application-examples"></a><span data-ttu-id="1fa67-105">Примеры приложений на C++ BITS</span><span class="sxs-lookup"><span data-stu-id="1fa67-105">BITS C++ Application Examples</span></span>

<span data-ttu-id="1fa67-106">Примеры приложений фоновая интеллектуальная служба передачи (BITS) в этом разделе написаны на C++.</span><span class="sxs-lookup"><span data-stu-id="1fa67-106">The Background Intelligent Transfer Service (BITS) application examples in this section are written in C++.</span></span> <span data-ttu-id="1fa67-107">Они демонстрируют ряд задач, которые можно выполнить с помощью функций службы BITS.</span><span class="sxs-lookup"><span data-stu-id="1fa67-107">They demonstrate a range of tasks that can be completed by using BITS features.</span></span> <span data-ttu-id="1fa67-108">Каждое приложение разделено на несколько шагов.</span><span class="sxs-lookup"><span data-stu-id="1fa67-108">Each application is separated into a series of steps.</span></span>

<span data-ttu-id="1fa67-109">В следующей таблице перечислены примеры C++ в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1fa67-109">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="1fa67-110">Пример</span><span class="sxs-lookup"><span data-stu-id="1fa67-110">Example</span></span>                                                                                                                                                            | <span data-ttu-id="1fa67-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1fa67-111">Description</span></span>                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fa67-112">Пример. Общие классы</span><span class="sxs-lookup"><span data-stu-id="1fa67-112">Example: Common Classes</span></span>](common-classes.md)                                                                                                                      | <span data-ttu-id="1fa67-113">Этот пример содержит общие классы, которые используются для примеров в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1fa67-113">This example contains common classes that are used for the examples in this section.</span></span> <span data-ttu-id="1fa67-114">Эти общие классы включают класс обратного вызова, класс универсальной ошибки и вспомогательный класс получения ресурсов для функции [COINITIALIZEEX](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) com.</span><span class="sxs-lookup"><span data-stu-id="1fa67-114">These common classes include a callback class, a generic error class, and a resource acquisition helper class for the COM [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> |
| [<span data-ttu-id="1fa67-115">Пример. Указание учетных данных проверки подлинности сервера для задания передачи BITS</span><span class="sxs-lookup"><span data-stu-id="1fa67-115">Example: Specifying Server Authentication Credentials for a BITS Transfer Job</span></span>](example-specifying-server-authentication-credentials-for-a-bits-transfer-job-.md) | <span data-ttu-id="1fa67-116">В этом примере получается схема авторизации и учетные данные пользователя, создается задание передачи BITS, устанавливаются учетные данные для задания и отслеживаются состояние задания.</span><span class="sxs-lookup"><span data-stu-id="1fa67-116">This example gets the authorization scheme and credentials from the user, creates a BITS transfer job, sets the credentials for the job, and monitors the status of the job.</span></span>                                                                                                               |
| [<span data-ttu-id="1fa67-117">Пример. Использование кодирования проверки подлинности SSPI с BITS.</span><span class="sxs-lookup"><span data-stu-id="1fa67-117">Example: Using SSPI Authentication Encoding with BITS.</span></span>](example-using-sspi-authentication-encoding-with-bits.md)                                                 | <span data-ttu-id="1fa67-118">В этом примере демонстрируется использование проверки подлинности с помощью интерфейса SSPI и BITS для получения учетных данных от пользователя, кодирования учетных данных и установки закодированных учетных данных для задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="1fa67-118">This example demonstrates the use of Security Support Provider Interface (SSPI) authentication and BITS to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span>                                                                |
| [<span data-ttu-id="1fa67-119">Пример. Добавление вспомогательного маркера в задание передачи BITS</span><span class="sxs-lookup"><span data-stu-id="1fa67-119">Example: Adding a Helper Token to a BITS Transfer Job</span></span>](example-adding-a-helper-token-to-a-bits-transfer-job-.md)                                                 | <span data-ttu-id="1fa67-120">В этом примере создается задание передачи BITS, а в задание добавляется второй набор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1fa67-120">This example creates a BITS transfer job and adds a second set of credentials to the job.</span></span>                                                                                                                                                                                                  |



 

 

 