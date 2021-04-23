---
description: В этом разделе описывается выполнение базовых задач программирования с помощью API цифровой подписи XPS.
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: Распространенные задачи по программированию цифровых подписей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498105"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="03c2c-103">Распространенные задачи по программированию цифровых подписей</span><span class="sxs-lookup"><span data-stu-id="03c2c-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="03c2c-104">В этом разделе описывается выполнение базовых задач программирования с помощью API цифровой подписи XPS.</span><span class="sxs-lookup"><span data-stu-id="03c2c-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="03c2c-105">Задания</span><span class="sxs-lookup"><span data-stu-id="03c2c-105">Tasks</span></span>

-   [<span data-ttu-id="03c2c-106">Инициализация диспетчера сигнатур</span><span class="sxs-lookup"><span data-stu-id="03c2c-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="03c2c-107">Подписать документ</span><span class="sxs-lookup"><span data-stu-id="03c2c-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="03c2c-108">Добавление запроса подписи в документ XPS</span><span class="sxs-lookup"><span data-stu-id="03c2c-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="03c2c-109">Проверка подписей документов</span><span class="sxs-lookup"><span data-stu-id="03c2c-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="03c2c-110">Отказ от ответственности</span><span class="sxs-lookup"><span data-stu-id="03c2c-110">Disclaimer</span></span>

<span data-ttu-id="03c2c-111">Примеры кода не предназначены для завершения и работы программ.</span><span class="sxs-lookup"><span data-stu-id="03c2c-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="03c2c-112">Примеры кода, упоминаемые на этой странице, например не выполняют проверку параметров, проверку ошибок, завершение управления памятью или ресурсами, а также обработку ошибок.</span><span class="sxs-lookup"><span data-stu-id="03c2c-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="03c2c-113">Используйте эти примеры в качестве отправной точки, а затем добавьте необходимый код для создания надежного приложения.</span><span class="sxs-lookup"><span data-stu-id="03c2c-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="03c2c-114">Дополнительные сведения о возвращаемых значениях **HRESULT** и стратегиях обработки ошибок см. [в разделе Обработка ошибок в com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="03c2c-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="03c2c-115">Для ясности в этих примерах кода используются очень простые сценарии документов и подписи XPS, которые могут быть недостаточно сложными в соответствии с вашими потребностями.</span><span class="sxs-lookup"><span data-stu-id="03c2c-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 
