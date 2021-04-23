---
description: Если планируется связать один или несколько типов файлов с новым приложением, необходимо определить идентификатор ProgID для каждого типа файлов, который необходимо связать с приложением.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Как зарегистрировать тип файла для нового приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985424"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a><span data-ttu-id="fae0f-103">Как зарегистрировать тип файла для нового приложения</span><span class="sxs-lookup"><span data-stu-id="fae0f-103">How to Register a File Type for a New Application</span></span>

<span data-ttu-id="fae0f-104">Если планируется связать один или несколько типов файлов с новым приложением, необходимо определить идентификатор ProgID для каждого типа файлов, который необходимо связать с приложением.</span><span class="sxs-lookup"><span data-stu-id="fae0f-104">If you plan to associate one or more file types with a new application, you must define a ProgID for each file type that you want to associate with the application.</span></span>

<span data-ttu-id="fae0f-105">Чтобы создать идентификатор ProgID для каждого уникального типа файла, обрабатываемого приложением, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fae0f-105">To create a ProgID for each unique file type that your application handles, use these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="fae0f-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="fae0f-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="fae0f-107">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="fae0f-107">Step 1:</span></span>

<span data-ttu-id="fae0f-108">Обратите внимание, что некоторые типы файлов имеют несколько расширений, которые указывают на один и тот же идентификатор ProgID; Например:</span><span class="sxs-lookup"><span data-stu-id="fae0f-108">Note that some file types have multiple extensions that point to the same ProgID; for example:</span></span>

-   <span data-ttu-id="fae0f-109">**HKey \_ \_Корневые классы** \\ **app. JPEG** (ваш идентификатор ProgID)</span><span class="sxs-lookup"><span data-stu-id="fae0f-109">**HKEY\_CLASSES\_ROOT**\\**App.jpeg** (your ProgID)</span></span>
-   <span data-ttu-id="fae0f-110">**HKey \_ Классы \_ root** \\ **. jpg** = App. JPEG (сопоставления типов файлов)</span><span class="sxs-lookup"><span data-stu-id="fae0f-110">**HKEY\_CLASSES\_ROOT**\\ **.jpg** = App.jpeg (the file type mappings)</span></span>
-   <span data-ttu-id="fae0f-111">**HKey \_ Классы \_ root** \\ **. JPEG** = App. JPEG</span><span class="sxs-lookup"><span data-stu-id="fae0f-111">**HKEY\_CLASSES\_ROOT**\\ **.jpeg** = App.jpeg</span></span>

### <a name="step-2"></a><span data-ttu-id="fae0f-112">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="fae0f-112">Step 2:</span></span>

<span data-ttu-id="fae0f-113">Удалите значения ProgID при установке и удалении программы.</span><span class="sxs-lookup"><span data-stu-id="fae0f-113">Remove the ProgID values when you install and uninstall your program.</span></span>

### <a name="step-3"></a><span data-ttu-id="fae0f-114">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="fae0f-114">Step 3:</span></span>

<span data-ttu-id="fae0f-115">Не изменяйте сопоставления типов файлов во время удаления.</span><span class="sxs-lookup"><span data-stu-id="fae0f-115">Leave the file type mappings unchanged at uninstall time.</span></span> <span data-ttu-id="fae0f-116">Это работает, поскольку сопоставления типов файлов хранятся для каждого пользователя в \_ классах hKey \_ root \\ . ext, а система определяет случай, когда значение ProgID отсутствует, и игнорирует его.</span><span class="sxs-lookup"><span data-stu-id="fae0f-116">Doing so works because file type mappings are stored per user in HKEY\_CLASSES\_ROOT\\.ext, and the system identifies the case where the ProgID value is missing and ignores it.</span></span> <span data-ttu-id="fae0f-117">При неизменном сопоставлении типов файлов не требуется использовать условный код, который удаляет сопоставление типов файлов, только если значение по-прежнему указывает на идентификатор ProgID.</span><span class="sxs-lookup"><span data-stu-id="fae0f-117">Leaving file type mappings unchanged avoids the need to have conditional code that only removes the file type mapping if the value still points to your ProgID.</span></span> <span data-ttu-id="fae0f-118">Важно избегать этого в случаях, когда оно могло быть изменено другим приложением, и таким образом нельзя легко удалить это значение.</span><span class="sxs-lookup"><span data-stu-id="fae0f-118">It is important to avoid doing so in cases where it might have been changed by another application and you thus cannot easily remove the value.</span></span>

### <a name="step-4"></a><span data-ttu-id="fae0f-119">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="fae0f-119">Step 4:</span></span>

<span data-ttu-id="fae0f-120">Укажите уникальное значение для описания типа файлов ProgID, выполнив одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="fae0f-120">Specify a unique value for the file type description of each file type ProgID by doing one of the following:</span></span>

-   <span data-ttu-id="fae0f-121">Оставьте значение ProgID по умолчанию пустым, в этом случае система использует файл. ext.</span><span class="sxs-lookup"><span data-stu-id="fae0f-121">Leave the default value of the ProgID empty, in which case the system uses the .ext file.</span></span>
-   <span data-ttu-id="fae0f-122">Предоставьте локализованное значение через Фриендлитипенаме и для совместимости с старыми приложениями, которые напрямую считывают реестр, обязательно укажите значение ProgID по умолчанию в качестве описания типа файла (то есть используйте то же значение, которое указано в Фриендлитипенаме в английском ресурсе).</span><span class="sxs-lookup"><span data-stu-id="fae0f-122">Provide a localized value via FriendlyTypeName and, for compatibility with old applications that read the registry directly, be sure to provide the default value of the ProgID as the file type description (that is, use the same value that is referred to by the FriendlyTypeName in the English resource).</span></span>

## <a name="remarks"></a><span data-ttu-id="fae0f-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="fae0f-123">Remarks</span></span>

<span data-ttu-id="fae0f-124">Если вы планируете связать файл с существующим приложением, то в реестре необходимо указать идентификатор ProgID приложения.</span><span class="sxs-lookup"><span data-stu-id="fae0f-124">If you plan to associate the file with an existing application, locate an application ProgID in the registry.</span></span> <span data-ttu-id="fae0f-125">Дополнительные сведения см. в разделе [типы файлов](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="fae0f-125">For more information, see [File Types](fa-file-types.md).</span></span>

 

 



