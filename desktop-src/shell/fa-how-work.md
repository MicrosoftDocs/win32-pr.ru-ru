---
description: Сопоставления файлов определяют, как оболочка обрабатывает тип файла в системе.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Как работают сопоставления файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264440"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="2d4d8-103">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-103">How File Associations Work</span></span>

<span data-ttu-id="2d4d8-104">Сопоставления файлов определяют, как оболочка обрабатывает [Тип файла](fa-file-types.md) в системе.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="2d4d8-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d4d8-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2d4d8-106">О сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="2d4d8-107">При необходимости реализации или изменения сопоставлений файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="2d4d8-108">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="2d4d8-109">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2d4d8-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="2d4d8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="2d4d8-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="2d4d8-111">О сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-111">About File Associations</span></span>

<span data-ttu-id="2d4d8-112">Взаимосвязи файлов управляют следующими функциональными возможностями:</span><span class="sxs-lookup"><span data-stu-id="2d4d8-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="2d4d8-113">Какое приложение запускается при двойном щелчке файла пользователем.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="2d4d8-114">Значок, который отображается для файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="2d4d8-115">Тип файла, отображаемый при просмотре в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="2d4d8-116">Команды, отображаемые в контекстном меню файла.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="2d4d8-117">Другие функции пользовательского интерфейса, такие как подсказки, сведения о плитках и область сведений.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="2d4d8-118">Разработчики приложений могут использовать сопоставления файлов для управления тем, как оболочка обрабатывает пользовательские типы файлов, или для связывания приложения с существующими типами файлов.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="2d4d8-119">Например, при установке приложения приложение может проверить наличие существующих сопоставлений файлов и либо создать, либо переопределить эти сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="2d4d8-120">Пользователи могут управлять некоторыми аспектами сопоставления файлов для настройки того, как оболочка обрабатывает тип файла либо с помощью команды **Открыть с** помощью пользовательского интерфейса, либо путем редактирования реестра.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="2d4d8-121">В окне проводника Windows, показанном на снимке экрана ниже, оболочка отображает разные значки для каждого файла в зависимости от значка, связанного с типом файла.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="2d4d8-122">Если пользователь дважды щелкает **точечный рисунок образца** файла, оболочка запускает Paint и использует его для открытия файла, так как в этой системе программа Paint связана с BMP-файлами.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="2d4d8-123">Пользователи могут управлять этими действиями с помощью сопоставлений файлов.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-123">People can control these actions using file associations.</span></span>

![Иллюстрация работы взаимосвязей файлов на практике](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="2d4d8-125">При необходимости реализации или изменения сопоставлений файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="2d4d8-126">Приложения могут использовать файлы для различных целей: некоторые файлы используются исключительно приложением и обычно недоступны пользователям, в то время как другие файлы создаются пользователем и часто открываются, ищутся и просматриваются в оболочке.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="2d4d8-127">Если пользовательский тип файлов не используется исключительно приложением, для него следует реализовать сопоставление файлов.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="2d4d8-128">Как правило, реализуйте сопоставления файлов для пользовательского типа файлов, если предполагается, что пользователь напрямую взаимодействует с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="2d4d8-129">Это включает использование оболочки для просмотра и открытия файлов, поиска содержимого или свойств файлов, а также предварительного просмотра файлов.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="2d4d8-130">Если приложение обрабатывает существующий тип файлов, не изменяйте сопоставление файлов, если вы не хотите изменить способ обработки оболочкой всех файлов этого типа.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="2d4d8-131">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-131">How File Associations Work</span></span>

<span data-ttu-id="2d4d8-132">Файлы представляются в оболочке как элементы оболочки.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="2d4d8-133">Для управления сопоставлениями файлов разработчики приложений могут регистрировать сопоставление между типом файла и обработчиками (COM-объектами, которые предоставляют функциональные возможности для элементов оболочки типа файла).</span><span class="sxs-lookup"><span data-stu-id="2d4d8-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="2d4d8-134">Когда оболочке необходимо запрашивать сопоставление файлов типа файлов, он создает массив разделов реестра, содержащий ассоциации для типа файла, и проверяет эти ключи для использования соответствующих сопоставлений файлов.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d4d8-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2d4d8-135">Additional Resources</span></span>

-   <span data-ttu-id="2d4d8-136">Концептуальные сведения о сопоставлении файлов см. в разделе [Обзор команд и сопоставлений файлов](fa-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="2d4d8-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d4d8-137">См. также</span><span class="sxs-lookup"><span data-stu-id="2d4d8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d4d8-138">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="2d4d8-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-139">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-140">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="2d4d8-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-141">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-142">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="2d4d8-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-143">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="2d4d8-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-144">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="2d4d8-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="2d4d8-145">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="2d4d8-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



