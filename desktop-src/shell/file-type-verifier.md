---
description: Средство проверки типа файлов — это инструмент, который позволяет независимым поставщикам программного обеспечения проверить, правильно ли реализованы их уникальные типы файлов.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Средство проверки типов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909567"
---
# <a name="file-type-verifier"></a><span data-ttu-id="a1dd2-103">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-103">File Type Verifier</span></span>

<span data-ttu-id="a1dd2-104">Средство проверки типа файлов — это инструмент, который позволяет независимым поставщикам программного обеспечения проверить, правильно ли реализованы их уникальные типы файлов.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="a1dd2-105">Высококачественные реализации обработчиков типов файлов очень важны для удобства работы пользователей, так как пользователи взаимодействуют с форматом файлов различными способами в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="a1dd2-106">Пользователи могут выполнять полнотекстовый поиск, сортировать по пользовательским метаданным или просматривать насыщенные эскизы и просматривать формат файла.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="a1dd2-107">Инструкции по использованию средства проверки типов файлов см. в разделе [как использовать файл проверки типов](how-to-use-the-file-type-verifier.md).</span><span class="sxs-lookup"><span data-stu-id="a1dd2-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="a1dd2-108">О средстве проверки типа файлов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="a1dd2-109">Средство проверки типов файлов — это программа, которая доступна в составе [пакета SDK для Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1dd2-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1dd2-110">Она призвана помочь разработчикам, создающим пользовательские [типы файлов](fa-file-types.md) Windows для обнаружения потенциальных проблем с типами файлов.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="a1dd2-111">Хотя средство проверки типов файлов выполняется только в Windows 7 и более поздних версиях, правила, применяемые средством проверки типов файлов, применяются ко всем версиям Windows, в которых доступны функции, которые он проверяет.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="a1dd2-112">Средство проверки типов файлов выполняет несколько тестов для типа файлов, чтобы убедиться, что он правильно зарегистрирован, и что он предоставляет [обработчики соответствующих типов файлов](fa-file-extensions.md) для правильного вывода типа файла в проводнике Windows и, если это уместно, поддерживает индексирование содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="a1dd2-113">Средство проверки типов файлов проверяет следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="a1dd2-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="a1dd2-114">Обработчики просмотра</span><span class="sxs-lookup"><span data-stu-id="a1dd2-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="a1dd2-115">Обработчики эскизов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="a1dd2-116">Обработчики свойств</span><span class="sxs-lookup"><span data-stu-id="a1dd2-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="a1dd2-117">Обработчики команд</span><span class="sxs-lookup"><span data-stu-id="a1dd2-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="a1dd2-118">Фильтры (IFilter)</span><span class="sxs-lookup"><span data-stu-id="a1dd2-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="a1dd2-119">Связи типов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="a1dd2-120">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="a1dd2-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="a1dd2-121">Важные свойства</span><span class="sxs-lookup"><span data-stu-id="a1dd2-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="a1dd2-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a1dd2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1dd2-123">Использование средства проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-124">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="a1dd2-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-125">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-126">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-127">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="a1dd2-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-128">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="a1dd2-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-129">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="a1dd2-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-130">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="a1dd2-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="a1dd2-131">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="a1dd2-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
