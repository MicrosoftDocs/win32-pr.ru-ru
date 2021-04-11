---
description: В Windows Vista и более поздних версиях метаданные стали центральным способом организации таких элементов, как файлы, электронная почта или контакты.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Реализация обработчиков свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265496"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="266ea-103">Реализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-103">Implementing Property Handlers</span></span>

<span data-ttu-id="266ea-104">В Windows Vista и более поздних версиях метаданные стали центральным способом организации таких элементов, как файлы, электронная почта или контакты.</span><span class="sxs-lookup"><span data-stu-id="266ea-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="266ea-105">Чтобы включить систему, в которой можно выполнять поиск элементов на основе их метаданных, а пользователи могут читать или записывать эти метаданные, в Windows Vista появилась новая система свойств.</span><span class="sxs-lookup"><span data-stu-id="266ea-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="266ea-106">Метаданные в этой системе представлены расширяемым набором свойств.</span><span class="sxs-lookup"><span data-stu-id="266ea-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="266ea-107">В этом наборе разделов описывается создание обработчика, который считывает и записывает свойства в файловый поток и из него.</span><span class="sxs-lookup"><span data-stu-id="266ea-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="266ea-108">Эти обработчики называются обработчиками свойств, каждый из которых связан с заданными типами файлов, определяемыми расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="266ea-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="266ea-109">В следующих разделах рассматриваются требования и стратегии, связанные с определением свойств и обработчиков свойств.</span><span class="sxs-lookup"><span data-stu-id="266ea-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="266ea-110">Основные сведения о обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="266ea-111">Использование имен видов</span><span class="sxs-lookup"><span data-stu-id="266ea-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="266ea-112">Использование списков свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="266ea-113">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="266ea-114">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="266ea-115">Рекомендации и вопросы и ответы по обработчикам свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="266ea-116">См. также</span><span class="sxs-lookup"><span data-stu-id="266ea-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="266ea-117">Создание пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="266ea-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="266ea-118">Схема описания свойства</span><span class="sxs-lookup"><span data-stu-id="266ea-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
