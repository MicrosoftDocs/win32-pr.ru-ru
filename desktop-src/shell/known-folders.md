---
description: В Windows Vista появились новые сценарии хранения данных и новое пространство имен профилей пользователей.
title: Известные папки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985781"
---
# <a name="known-folders"></a><span data-ttu-id="f0725-103">Известные папки</span><span class="sxs-lookup"><span data-stu-id="f0725-103">Known Folders</span></span>

<span data-ttu-id="f0725-104">В Windows Vista появились новые сценарии хранения данных и новое пространство имен профилей пользователей.</span><span class="sxs-lookup"><span data-stu-id="f0725-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="f0725-105">Для решения этих новых факторов была заменена более старая система, ссылающаяся на стандартные папки по значению [**CSid**](csidl.md) .</span><span class="sxs-lookup"><span data-stu-id="f0725-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="f0725-106">Начиная с Windows Vista, на эти папки ссылается новый набор значений GUID, именуемый идентификаторами известных папок.</span><span class="sxs-lookup"><span data-stu-id="f0725-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="f0725-107">Система известных папок предоставляет следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="f0725-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="f0725-108">Независимые поставщики программного обеспечения могут расширять набор известных идентификаторов папок своим собственным.</span><span class="sxs-lookup"><span data-stu-id="f0725-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="f0725-109">Они могут определять папки, давать им идентификаторы и регистрировать их в системе.</span><span class="sxs-lookup"><span data-stu-id="f0725-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="f0725-110">Не удалось расширить значения CSID.</span><span class="sxs-lookup"><span data-stu-id="f0725-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="f0725-111">Можно перечислить все известные папки в системе.</span><span class="sxs-lookup"><span data-stu-id="f0725-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="f0725-112">API не предоставил эти функции для значений CSID.</span><span class="sxs-lookup"><span data-stu-id="f0725-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="f0725-113">Дополнительные сведения см. в разделе [**икновнфолдерманажер:: жетфолдеридс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .</span><span class="sxs-lookup"><span data-stu-id="f0725-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="f0725-114">Известная папка, добавленная независимым поставщиком программного обеспечения, может добавлять пользовательские свойства, позволяющие объяснить его назначение и предполагаемое использование.</span><span class="sxs-lookup"><span data-stu-id="f0725-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="f0725-115">Многие известные папки могут перенаправляться в новые расположения, включая сетевые расположения.</span><span class="sxs-lookup"><span data-stu-id="f0725-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="f0725-116">В системе CSID можно перенаправить только папку **«Мои документы** ».</span><span class="sxs-lookup"><span data-stu-id="f0725-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="f0725-117">Известные папки могут иметь пользовательские обработчики для использования во время создания или удаления.</span><span class="sxs-lookup"><span data-stu-id="f0725-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="f0725-118">Система и API-интерфейсы CSID, которые используют значения CSID, все еще поддерживаются для совместимости.</span><span class="sxs-lookup"><span data-stu-id="f0725-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="f0725-119">Однако не рекомендуется использовать их в любых новых разработках.</span><span class="sxs-lookup"><span data-stu-id="f0725-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="f0725-120">В следующих разделах рассматриваются особенности системы известных папок.</span><span class="sxs-lookup"><span data-stu-id="f0725-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="f0725-121">Работа с известными папками в приложениях</span><span class="sxs-lookup"><span data-stu-id="f0725-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="f0725-122">Расширение известных папок с помощью пользовательских папок</span><span class="sxs-lookup"><span data-stu-id="f0725-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="f0725-123">**кновнфолдерид**</span><span class="sxs-lookup"><span data-stu-id="f0725-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="f0725-124">На следующих справочных страницах объясняются функции известных папок Win32, которые можно использовать для получения расположения известных папок или перенаправлять их в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="f0725-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="f0725-125">Эти функции заменяют старые функции Win32.</span><span class="sxs-lookup"><span data-stu-id="f0725-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="f0725-126">Новые функции предоставляют эквивалентное поведение старым функциям, но каждая новая функция также дублируется API-интерфейсом модели компонентов (COM).</span><span class="sxs-lookup"><span data-stu-id="f0725-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="f0725-127">Новая функция</span><span class="sxs-lookup"><span data-stu-id="f0725-127">New Function</span></span>                                             | <span data-ttu-id="f0725-128">Меняющей</span><span class="sxs-lookup"><span data-stu-id="f0725-128">Replaces</span></span>                                           | <span data-ttu-id="f0725-129">Эквивалент COM</span><span class="sxs-lookup"><span data-stu-id="f0725-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="f0725-130">**шжеткновнфолдерпас**</span><span class="sxs-lookup"><span data-stu-id="f0725-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="f0725-131">**шжетфолдерпас**</span><span class="sxs-lookup"><span data-stu-id="f0725-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="f0725-132">**Икновнфолдер:: path**</span><span class="sxs-lookup"><span data-stu-id="f0725-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="f0725-133">**шжеткновнфолдеридлист**</span><span class="sxs-lookup"><span data-stu-id="f0725-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="f0725-134">**шжетфолдерлокатион**</span><span class="sxs-lookup"><span data-stu-id="f0725-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="f0725-135">**Икновнфолдер:: Жетидлист**</span><span class="sxs-lookup"><span data-stu-id="f0725-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="f0725-136">**шсеткновнфолдерпас**</span><span class="sxs-lookup"><span data-stu-id="f0725-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="f0725-137">**шсетфолдерпас**</span><span class="sxs-lookup"><span data-stu-id="f0725-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="f0725-138">**Икновнфолдер:: Сетпас**</span><span class="sxs-lookup"><span data-stu-id="f0725-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="f0725-139">На следующих справочных страницах объясняются API-интерфейсы известных папок COM, которые предоставляют все функции API Win32, перечисленные выше, а также добавляют возможность перечисления всех известных папок, доступа к известным свойствам папок и расширения стандартного набора известных папок.</span><span class="sxs-lookup"><span data-stu-id="f0725-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="f0725-140">**икновнфолдер**</span><span class="sxs-lookup"><span data-stu-id="f0725-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="f0725-141">**икновнфолдерманажер**</span><span class="sxs-lookup"><span data-stu-id="f0725-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="f0725-142">Пример на языке C++, демонстрирующий известные API папки, входит в состав пакета средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="f0725-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f0725-143">После установки Windows SDK на компьютере этот пример можно найти в разделе% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ винуи \\ Shell \\ аппплатформ \\ кновнфолдерс.</span><span class="sxs-lookup"><span data-stu-id="f0725-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0725-144">См. также</span><span class="sxs-lookup"><span data-stu-id="f0725-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f0725-145">[Пример: известные папки](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0725-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
