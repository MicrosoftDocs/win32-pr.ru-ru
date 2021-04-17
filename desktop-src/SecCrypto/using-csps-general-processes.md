---
description: При использовании поставщиков служб шифрования CSP учитывайте следующие соглашения.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Использование CSP: общие процессы'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682982"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="3d5c4-103">Использование CSP: общие процессы</span><span class="sxs-lookup"><span data-stu-id="3d5c4-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="3d5c4-104">При использовании [*поставщиков служб шифрования*](../secgloss/c-gly.md) CSP учитывайте следующие соглашения.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="3d5c4-105">Кэширование закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="3d5c4-105">Private Key Caching</span></span>

<span data-ttu-id="3d5c4-106">CSP может кэшировать некоторые [*закрытые ключи*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3d5c4-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="3d5c4-107">Это кэширование закрытых ключей можно контролировать в глобальном, но не на основе конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="3d5c4-108">Кэширование изменений выполняется путем изменения определенных параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="3d5c4-109">Дополнительные сведения см. в разделе [**константы кэширования закрытых ключей**](private-key-caching-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d5c4-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="3d5c4-110">Примеры соглашений о коде</span><span class="sxs-lookup"><span data-stu-id="3d5c4-110">Example Code Conventions</span></span>

<span data-ttu-id="3d5c4-111">Для более краткого и удобочитаемого кода некоторые принципы хорошего программирования не всегда следуют в примерах.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="3d5c4-112">В частности:</span><span class="sxs-lookup"><span data-stu-id="3d5c4-112">In particular:</span></span>

-   <span data-ttu-id="3d5c4-113">Отображаются только ограниченные ответы на ошибки.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-113">Only limited error responses are shown.</span></span> <span data-ttu-id="3d5c4-114">Правильно написанные, полные программы проверяют возвращенные коды ошибок и выполняют соответствующие действия при обнаружении ошибки.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="3d5c4-115">Выполняется только ограниченное управление памятью и ресурсами.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="3d5c4-116">Правильно написанные, законченные программы удаляют все ключи и [*хэши*](../secgloss/h-gly.md), освобождают все выделенные памяти, закрывают все файлы и выпускают все дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="3d5c4-117">Эти примеры предоставляют только ограниченные демонстрации использования функций, выполняющих эти задачи.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="3d5c4-118">Эти примеры не выполняют задачи по управлению ресурсами памяти или ресурсов в случае завершения программы из-за ошибок.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="3d5c4-119">В следующих разделах представлены общие сведения о примерах процедур, а также примеры кода.</span><span class="sxs-lookup"><span data-stu-id="3d5c4-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="3d5c4-120">Получение данных неизвестной длины</span><span class="sxs-lookup"><span data-stu-id="3d5c4-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="3d5c4-121">Перечисление поддерживаемых протоколов</span><span class="sxs-lookup"><span data-stu-id="3d5c4-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
