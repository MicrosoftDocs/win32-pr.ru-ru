---
description: Воспринимаемый тип — это категория типов файлов, которая позволяет выбрать тип файла для Windows (и приложений) как образ, аудио, документ или другой тип.
title: Воспринимаемые типы (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998006"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="dda53-103">Воспринимаемые типы (оболочка Windows)</span><span class="sxs-lookup"><span data-stu-id="dda53-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="dda53-104">Воспринимаемый тип — это категория типов файлов, которая позволяет выбрать тип файла для Windows (и приложений) как образ, аудио, документ или другой тип.</span><span class="sxs-lookup"><span data-stu-id="dda53-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="dda53-105">Наблюдаемые типы используются в нескольких целях, включая определение типа папки, которая затем используется для задания параметров представления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dda53-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="dda53-106">Например, папка с файлами, имеющими изображение распознанного типа, назначается режиму просмотра по умолчанию для эскизов.</span><span class="sxs-lookup"><span data-stu-id="dda53-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="dda53-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="dda53-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="dda53-108">О наблюдаемых типах</span><span class="sxs-lookup"><span data-stu-id="dda53-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="dda53-109">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dda53-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="dda53-110">См. также</span><span class="sxs-lookup"><span data-stu-id="dda53-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="dda53-111">О наблюдаемых типах</span><span class="sxs-lookup"><span data-stu-id="dda53-111">About Perceived Types</span></span>

<span data-ttu-id="dda53-112">Распознанные типы, определенные как значения PerceivedType, похожи на типы файлов, за исключением того, что они ссылаются на обширные категории типов файлов, а не конкретные типы файлов.</span><span class="sxs-lookup"><span data-stu-id="dda53-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="dda53-113">Например, изображения, текстовые, звуковые и сжатые типы считаются распознанными.</span><span class="sxs-lookup"><span data-stu-id="dda53-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="dda53-114">Типы файлов (обычно общедоступные типы файлов) могут быть назначены воспринимаемым типом, и их всегда следует назначать каждый раз, когда есть подходящий.</span><span class="sxs-lookup"><span data-stu-id="dda53-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="dda53-115">Например, файлы изображений типа. bmp,. PNG,. jpg и. GIF также имеют распознанный тип Image.</span><span class="sxs-lookup"><span data-stu-id="dda53-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="dda53-116">По умолчанию распознанные типы выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="dda53-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="dda53-117">Папка</span><span class="sxs-lookup"><span data-stu-id="dda53-117">Folder</span></span>
-   <span data-ttu-id="dda53-118">Текст</span><span class="sxs-lookup"><span data-stu-id="dda53-118">Text</span></span>
-   <span data-ttu-id="dda53-119">Образ —</span><span class="sxs-lookup"><span data-stu-id="dda53-119">Image</span></span>
-   <span data-ttu-id="dda53-120">звук;</span><span class="sxs-lookup"><span data-stu-id="dda53-120">Audio</span></span>
-   <span data-ttu-id="dda53-121">Видео</span><span class="sxs-lookup"><span data-stu-id="dda53-121">Video</span></span>
-   <span data-ttu-id="dda53-122">Compressed</span><span class="sxs-lookup"><span data-stu-id="dda53-122">Compressed</span></span>
-   <span data-ttu-id="dda53-123">Документ</span><span class="sxs-lookup"><span data-stu-id="dda53-123">Document</span></span>
-   <span data-ttu-id="dda53-124">Система</span><span class="sxs-lookup"><span data-stu-id="dda53-124">System</span></span>
-   <span data-ttu-id="dda53-125">Приложение</span><span class="sxs-lookup"><span data-stu-id="dda53-125">Application</span></span>
-   <span data-ttu-id="dda53-126">гамемедиа</span><span class="sxs-lookup"><span data-stu-id="dda53-126">Gamemedia</span></span>
-   <span data-ttu-id="dda53-127">Контакты</span><span class="sxs-lookup"><span data-stu-id="dda53-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dda53-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dda53-128">Additional Resources</span></span>

-   <span data-ttu-id="dda53-129">Сведения о регистрации наблюдаемых типов см. в разделе [Регистрация приложений](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="dda53-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="dda53-130">Список распознанных типов по умолчанию см. в разделе [**воспринимаемое**](/windows/win32/api/shtypes/ne-shtypes-perceived) перечисление.</span><span class="sxs-lookup"><span data-stu-id="dda53-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="dda53-131">Чтобы получить распознанный тип файла на основе расширения имени файла, см. раздел Функция [**ассокжетперцеиведтипе**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .</span><span class="sxs-lookup"><span data-stu-id="dda53-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dda53-132">См. также</span><span class="sxs-lookup"><span data-stu-id="dda53-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dda53-133">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="dda53-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="dda53-134">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="dda53-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="dda53-135">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="dda53-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="dda53-136">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="dda53-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="dda53-137">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="dda53-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="dda53-138">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="dda53-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="dda53-139">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="dda53-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="dda53-140">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="dda53-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



