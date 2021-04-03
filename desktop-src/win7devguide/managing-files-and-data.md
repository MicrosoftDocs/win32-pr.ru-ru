---
title: Управление файлами и данными
description: Пользователи имеют более простой доступ к файлам и данным в Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987664"
---
# <a name="managing-files-and-data"></a><span data-ttu-id="c964f-103">Управление файлами и данными</span><span class="sxs-lookup"><span data-stu-id="c964f-103">Managing Files and Data</span></span>

<span data-ttu-id="c964f-104">Пользователи имеют более простой доступ к файлам и данным в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c964f-104">Users have easier access to files and data in Windows 7.</span></span> <span data-ttu-id="c964f-105">Новые интерфейсы API делают файлы и представления более информативными, позволяя приложениям предоставлять в проводник Windows необходимые и отличительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c964f-105">New APIs make files and views more informative, enabling applications to deliver relevant and distinctive information to Windows Explorer.</span></span> <span data-ttu-id="c964f-106">Кроме того, приложения используют преимущества новой модели *библиотек* , полезное, более абстрактное понятие пространства для хранения данных пользователя, чем папки, и могут участвовать в общих библиотеках схожих типов файлов, совместно используемых различными приложениями.</span><span class="sxs-lookup"><span data-stu-id="c964f-106">In addition, applications benefit from the new *Libraries* model, a useful, more abstract notion of user storage space than folders, and can also participate in common libraries of similar file types that are shared by different applications.</span></span>

## <a name="libraries"></a><span data-ttu-id="c964f-107">Библиотеки</span><span class="sxs-lookup"><span data-stu-id="c964f-107">Libraries</span></span>

<span data-ttu-id="c964f-108">В Windows 7 представлена концепция *библиотек* в качестве назначений, где разработчики и конечные пользователи могут находить и упорядочивать свои данные в виде коллекций элементов, которые могут охватывать несколько расположений на локальном компьютере, а также на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="c964f-108">Windows 7 introduces the concept of *Libraries* as destinations where developers and end-users can find and organize their data as collections of items that can span multiple locations on the local computer as well as on remote computers.</span></span>

<span data-ttu-id="c964f-109">API-интерфейсы *библиотеки* предоставляют разработчикам простой способ создания приложений, которые создают, взаимодействуют с *библиотеками* и поддерживают их в качестве элементов первого класса в приложениях.</span><span class="sxs-lookup"><span data-stu-id="c964f-109">The *Library* APIs provide a straightforward way for developers to create applications that create, interact with, and support *Libraries* as first-class items within applications.</span></span> <span data-ttu-id="c964f-110">*Библиотеки* также можно выбрать с помощью диалогового окна Выбор папки.</span><span class="sxs-lookup"><span data-stu-id="c964f-110">*Libraries* can also be selected by using the folder picker dialog box.</span></span> <span data-ttu-id="c964f-111">Приложения могут перечислять соответствующие области библиотеки, а также использовать библиотеку непосредственно в качестве папки.</span><span class="sxs-lookup"><span data-stu-id="c964f-111">Applications can enumerate relevant library scopes, or they can use the library directly as a folder.</span></span> <span data-ttu-id="c964f-112">(См. раздел [библиотеки Windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) и [библиотеки Windows 7: ресурсы для разработчиков](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span><span class="sxs-lookup"><span data-stu-id="c964f-112">(See [Windows Libraries](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) and [Windows 7 Libraries: Developer Resources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span></span>

![Библиотека изображений Windows 7](images/windows7-10.jpg)

<span data-ttu-id="c964f-114">*Библиотека рисунков* отображает изображения независимо от того, где они хранятся</span><span class="sxs-lookup"><span data-stu-id="c964f-114">*Pictures Library* shows your pictures no matter where they are stored</span></span>

## <a name="file-formats-and-data-stores"></a><span data-ttu-id="c964f-115">Форматы файлов и хранилища данных</span><span class="sxs-lookup"><span data-stu-id="c964f-115">File Formats and Data Stores</span></span>

<span data-ttu-id="c964f-116">В Windows 7 проводник Windows упрощает управление файлами и манипуляции с пользователем несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="c964f-116">In Windows 7, Windows Explorer makes file management and manipulation easier for the user in several ways:</span></span>

-   <span data-ttu-id="c964f-117">Предварительная версия для типа файлов приложения становится более доступной с помощью новой кнопки, позволяющей пользователям отображать и скрывать область просмотра.</span><span class="sxs-lookup"><span data-stu-id="c964f-117">The preview for your application's file type is more accessible with a new button that lets users show and hide the preview pane.</span></span>
-   <span data-ttu-id="c964f-118">Впечатляющие визуальные стеки объединяют эскизные изображения для типов файлов в представлении.</span><span class="sxs-lookup"><span data-stu-id="c964f-118">Immersive visual stacks aggregate thumbnail images for file types in a view.</span></span>
-   <span data-ttu-id="c964f-119">Представления проводника Windows отображают полезную информацию на основе свойств, записанных с помощью обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="c964f-119">Windows Explorer views show useful information based on properties written with your property handler.</span></span>
-   <span data-ttu-id="c964f-120">Фрагменты документов и выделение вхождений. Используйте реализацию интерфейса **IFilter** , чтобы упростить поиск и поиск файлов.</span><span class="sxs-lookup"><span data-stu-id="c964f-120">Document snippets and hit highlighting use your **IFilter** interface implementation to make searching and finding files easier.</span></span>
-   <span data-ttu-id="c964f-121">Действия и команды контекстного меню проще, чем когда-либо, для реализации.</span><span class="sxs-lookup"><span data-stu-id="c964f-121">Context-menu verbs and commands are easier than ever to implement.</span></span>

<span data-ttu-id="c964f-122">Путем реализации всех соответствующих обработчиков формата для элементов, возвращаемых обработчиком протокола, результаты поиска из пользовательского хранилища данных могут иметь такой же формат, как результаты поиска из файлов.</span><span class="sxs-lookup"><span data-stu-id="c964f-122">By implementing all of the appropriate format handlers for the items returned from your protocol handler, search results from your custom data store can be as rich as search results from files.</span></span> <span data-ttu-id="c964f-123">Для обработчиков протоколов автоматически создаются *библиотеки* , чтобы пользователи могли легко ограничить область поиска.</span><span class="sxs-lookup"><span data-stu-id="c964f-123">*Libraries* are automatically created for your protocol handlers so users can scope their searches easily.</span></span> <span data-ttu-id="c964f-124">Логику создания *библиотек* можно легко настроить с помощью реестра.</span><span class="sxs-lookup"><span data-stu-id="c964f-124">And the logic for creating *Libraries* can be easily customized through the registry.</span></span> <span data-ttu-id="c964f-125">(См. раздел [Разработка фильтров для поиска Windows](../search/-search-3x-wds-extidx-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="c964f-125">(See [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span></span>

![Библиотека документов Windows 7](images/windows7-11.jpg)

<span data-ttu-id="c964f-127">В Windows 7 проводник Windows упрощает управление файлами и их обработку</span><span class="sxs-lookup"><span data-stu-id="c964f-127">In Windows 7, Windows Explorer makes file management and manipulation easier</span></span>

 

 