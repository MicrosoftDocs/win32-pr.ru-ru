---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Библиотека файлов заменяет папку документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912759"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="15828-103">Библиотека файлов заменяет папку документа</span><span class="sxs-lookup"><span data-stu-id="15828-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="15828-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="15828-104">Affected Platforms</span></span>

<span data-ttu-id="15828-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="15828-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="15828-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15828-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="15828-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="15828-107">Feature Impact</span></span>

<span data-ttu-id="15828-108">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="15828-108">**Severity** - Medium</span></span>  
<span data-ttu-id="15828-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="15828-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="15828-110">Описание</span><span class="sxs-lookup"><span data-stu-id="15828-110">Description</span></span>

<span data-ttu-id="15828-111">Библиотеки обеспечивают централизованную работу с папками для хранения файлов, поиска и доступа в нескольких расположениях, как локальных, так и удаленных.</span><span class="sxs-lookup"><span data-stu-id="15828-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="15828-112">Расположения по умолчанию, используемые общими диалоговыми файлами (например, Open и Save), были изменены из папки документов в библиотеку документов.</span><span class="sxs-lookup"><span data-stu-id="15828-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="15828-113">Пользовательский интерфейс не изменяется, но теперь пользователь сможет просматривать, просматривать и искать библиотеку с помощью различных представлений упорядочения.</span><span class="sxs-lookup"><span data-stu-id="15828-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="15828-114">Файлы будут сохраняться в папке сохранения по умолчанию, если пользователь не изменит расположение сохранения по умолчанию или не укажет другую папку.</span><span class="sxs-lookup"><span data-stu-id="15828-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="15828-115">Разработчики могут создавать собственные библиотеки или добавлять расположения в существующие библиотеки с помощью интерфейса Ишелллибрари.</span><span class="sxs-lookup"><span data-stu-id="15828-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="15828-116">Пользователи могут находить библиотеки с помощью известной системы папок (например, FOLDERID \_ документслибрари).</span><span class="sxs-lookup"><span data-stu-id="15828-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="15828-117">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="15828-117">Manifestation of Impact</span></span>

<span data-ttu-id="15828-118">Библиотека сама по себе является файлом, а не папкой.</span><span class="sxs-lookup"><span data-stu-id="15828-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="15828-119">Таким образом, операции с путями могут привести к ошибкам из-за попытки приложения объединить файлы в файлы.</span><span class="sxs-lookup"><span data-stu-id="15828-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="15828-120">Решение</span><span class="sxs-lookup"><span data-stu-id="15828-120">Solution</span></span>

<span data-ttu-id="15828-121">При использовании Ифиледиалог необходимо использовать метод «методом» вместо комбинации файлов «. Folder» и «ИмяФайла», как в предыдущих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="15828-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="15828-122">Используйте интерфейсы API оболочки, где это возможно, чтобы взаимодействовать с элементами в пространстве имен оболочки и управлять ими (например, интерфейса IShellItem).</span><span class="sxs-lookup"><span data-stu-id="15828-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="15828-123">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="15828-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="15828-124">Если вы хотите создать собственные библиотеки или добавить расположения в существующие библиотеки, необходимо использовать API Ишелллибрари.</span><span class="sxs-lookup"><span data-stu-id="15828-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="15828-125">Библиотеки сами являются папками оболочки, поэтому их можно перечислить так же, как и любую другую папку оболочки.</span><span class="sxs-lookup"><span data-stu-id="15828-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="15828-126">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="15828-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="15828-127">При использовании общего диалогового окна «файл» пользователи смогут сохранять данные непосредственно в своих библиотеках.</span><span class="sxs-lookup"><span data-stu-id="15828-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="15828-128">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="15828-128">Links to Other Resources</span></span>

-   <span data-ttu-id="15828-129">**Библиотеки Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="15828-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="15828-130">**Синхронизация с библиотекой:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="15828-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



