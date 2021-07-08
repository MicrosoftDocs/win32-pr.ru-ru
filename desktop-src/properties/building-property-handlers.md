---
description: Узнайте, как создать обработчик свойств, который считывает и записывает свойства в файловый поток и из него. Каждый обработчик связан с заданным типом файла.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Реализация обработчиков свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481839"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="bf12b-104">Реализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-104">Implementing Property Handlers</span></span>

<span data-ttu-id="bf12b-105">в Windows Vista и более поздних версиях метаданные становятся центральным способом организации таких элементов, как файлы, электронная почта или контакты.</span><span class="sxs-lookup"><span data-stu-id="bf12b-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="bf12b-106">чтобы включить систему, в которой можно выполнять поиск элементов на основе их метаданных, а пользователи могут читать или записывать эти метаданные, Windows в Vista появилась новая система свойств.</span><span class="sxs-lookup"><span data-stu-id="bf12b-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="bf12b-107">Метаданные в этой системе представлены расширяемым набором свойств.</span><span class="sxs-lookup"><span data-stu-id="bf12b-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="bf12b-108">В этом наборе разделов описывается создание обработчика, который считывает и записывает свойства в файловый поток и из него.</span><span class="sxs-lookup"><span data-stu-id="bf12b-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="bf12b-109">Эти обработчики называются обработчиками свойств, каждый из которых связан с заданными типами файлов, определяемыми расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="bf12b-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="bf12b-110">В следующих разделах рассматриваются требования и стратегии, связанные с определением свойств и обработчиков свойств.</span><span class="sxs-lookup"><span data-stu-id="bf12b-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="bf12b-111">Основные сведения о обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="bf12b-112">Использование имен видов</span><span class="sxs-lookup"><span data-stu-id="bf12b-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="bf12b-113">Использование списков свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="bf12b-114">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="bf12b-115">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="bf12b-116">Рекомендации и вопросы и ответы по обработчикам свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="bf12b-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bf12b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf12b-118">Создание пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="bf12b-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="bf12b-119">Схема описания свойства</span><span class="sxs-lookup"><span data-stu-id="bf12b-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
