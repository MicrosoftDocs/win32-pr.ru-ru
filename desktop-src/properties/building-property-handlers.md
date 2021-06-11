---
description: Узнайте, как создать обработчик свойств, который считывает и записывает свойства в файловый поток и из него. Каждый обработчик связан с заданным типом файла.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Реализация обработчиков свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989269"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="0be19-104">Реализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-104">Implementing Property Handlers</span></span>

<span data-ttu-id="0be19-105">В Windows Vista и более поздних версиях метаданные стали центральным способом организации таких элементов, как файлы, электронная почта или контакты.</span><span class="sxs-lookup"><span data-stu-id="0be19-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="0be19-106">Чтобы включить систему, в которой можно выполнять поиск элементов на основе их метаданных, а пользователи могут читать или записывать эти метаданные, в Windows Vista появилась новая система свойств.</span><span class="sxs-lookup"><span data-stu-id="0be19-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="0be19-107">Метаданные в этой системе представлены расширяемым набором свойств.</span><span class="sxs-lookup"><span data-stu-id="0be19-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="0be19-108">В этом наборе разделов описывается создание обработчика, который считывает и записывает свойства в файловый поток и из него.</span><span class="sxs-lookup"><span data-stu-id="0be19-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="0be19-109">Эти обработчики называются обработчиками свойств, каждый из которых связан с заданными типами файлов, определяемыми расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="0be19-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="0be19-110">В следующих разделах рассматриваются требования и стратегии, связанные с определением свойств и обработчиков свойств.</span><span class="sxs-lookup"><span data-stu-id="0be19-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="0be19-111">Основные сведения о обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="0be19-112">Использование имен видов</span><span class="sxs-lookup"><span data-stu-id="0be19-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="0be19-113">Использование списков свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="0be19-114">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="0be19-115">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="0be19-116">Рекомендации и вопросы и ответы по обработчикам свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="0be19-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0be19-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be19-118">Создание пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="0be19-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="0be19-119">Схема описания свойства</span><span class="sxs-lookup"><span data-stu-id="0be19-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
