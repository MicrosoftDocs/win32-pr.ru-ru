---
title: Функции ADSI
description: Active Directory интерфейсы служб предоставляют следующие вспомогательные функции клиентам, которые не используют автоматизацию.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI ADSI, ссылки, функции
- функции ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328443"
---
# <a name="adsi-functions"></a><span data-ttu-id="e3415-105">Функции ADSI</span><span class="sxs-lookup"><span data-stu-id="e3415-105">ADSI Functions</span></span>

<span data-ttu-id="e3415-106">Active Directory интерфейсы служб предоставляют следующие вспомогательные функции клиентам, которые не используют автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="e3415-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="e3415-107">Функция</span><span class="sxs-lookup"><span data-stu-id="e3415-107">Function</span></span>                                           | <span data-ttu-id="e3415-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e3415-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3415-109">**адсбуилденумератор**</span><span class="sxs-lookup"><span data-stu-id="e3415-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="e3415-110">Создает объект перечислителя для указанного объекта контейнера ADSI.</span><span class="sxs-lookup"><span data-stu-id="e3415-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="e3415-111">**адсбуилдвараррайинт**</span><span class="sxs-lookup"><span data-stu-id="e3415-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="e3415-112">Создает массив вариантов из массива **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="e3415-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="e3415-113">**адсбуилдвараррайстр**</span><span class="sxs-lookup"><span data-stu-id="e3415-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="e3415-114">Создает массив Variant из массива строк в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e3415-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="e3415-115">**адсенкодебинаридата**</span><span class="sxs-lookup"><span data-stu-id="e3415-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="e3415-116">Преобразует большой двоичный объект двоичных данных в формат, подходящий для фильтра поиска.</span><span class="sxs-lookup"><span data-stu-id="e3415-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="e3415-117">**адсенумератенекст**</span><span class="sxs-lookup"><span data-stu-id="e3415-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="e3415-118">Заполняет массив Variant элементами, полученными из указанного объекта перечислителя.</span><span class="sxs-lookup"><span data-stu-id="e3415-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="e3415-119">**адсфриенумератор**</span><span class="sxs-lookup"><span data-stu-id="e3415-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="e3415-120">Освобождает объект перечислителя, созданный ранее [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span><span class="sxs-lookup"><span data-stu-id="e3415-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="e3415-121">**адсжетластеррор**</span><span class="sxs-lookup"><span data-stu-id="e3415-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="e3415-122">Извлекает Последнее значение кода ошибки вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="e3415-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="e3415-123">**адсжетобжект**</span><span class="sxs-lookup"><span data-stu-id="e3415-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="e3415-124">Выполняет привязку к объекту ADSI, используя текущие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e3415-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="e3415-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="e3415-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="e3415-126">Выполняет привязку к объекту ADSI с использованием указанных учетных данных</span><span class="sxs-lookup"><span data-stu-id="e3415-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="e3415-127">**адссетластеррор**</span><span class="sxs-lookup"><span data-stu-id="e3415-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="e3415-128">Задает значение кода ошибки вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="e3415-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="e3415-129">**аллокадсмем**</span><span class="sxs-lookup"><span data-stu-id="e3415-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="e3415-130">Выделяет блок памяти.</span><span class="sxs-lookup"><span data-stu-id="e3415-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="e3415-131">**аллокадсстр**</span><span class="sxs-lookup"><span data-stu-id="e3415-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="e3415-132">Выделяет память для заданной строки.</span><span class="sxs-lookup"><span data-stu-id="e3415-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="e3415-133">**фриадсмем**</span><span class="sxs-lookup"><span data-stu-id="e3415-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="e3415-134">Освобождает память, выделенную [**аллокадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span><span class="sxs-lookup"><span data-stu-id="e3415-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="e3415-135">**фриадсстр**</span><span class="sxs-lookup"><span data-stu-id="e3415-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="e3415-136">Освобождает память, выделенную для заданной строки.</span><span class="sxs-lookup"><span data-stu-id="e3415-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="e3415-137">**реаллокадсмем**</span><span class="sxs-lookup"><span data-stu-id="e3415-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="e3415-138">Назначает существующее содержимое памяти только что созданному расположению в памяти.</span><span class="sxs-lookup"><span data-stu-id="e3415-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="e3415-139">**реаллокадсстр**</span><span class="sxs-lookup"><span data-stu-id="e3415-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="e3415-140">Заменяет существующую строку новой.</span><span class="sxs-lookup"><span data-stu-id="e3415-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="e3415-141">Следующие функции ADSI устарели.</span><span class="sxs-lookup"><span data-stu-id="e3415-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="e3415-142">Функция</span><span class="sxs-lookup"><span data-stu-id="e3415-142">Function</span></span>                                                  | <span data-ttu-id="e3415-143">Описание</span><span class="sxs-lookup"><span data-stu-id="e3415-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="e3415-144">**адсфриаллерроррекордс**</span><span class="sxs-lookup"><span data-stu-id="e3415-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="e3415-145">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-145">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-146">**адсдекодебинаридата**</span><span class="sxs-lookup"><span data-stu-id="e3415-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="e3415-147">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-147">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-148">**пропварианттоадстипе**</span><span class="sxs-lookup"><span data-stu-id="e3415-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="e3415-149">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-149">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-150">**адстипетопропвариант**</span><span class="sxs-lookup"><span data-stu-id="e3415-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="e3415-151">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-151">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-152">**адсфриадсвалуес**</span><span class="sxs-lookup"><span data-stu-id="e3415-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="e3415-153">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-153">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-154">**инитадсмем**</span><span class="sxs-lookup"><span data-stu-id="e3415-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="e3415-155">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-155">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-156">**ассертадсмемлеакс**</span><span class="sxs-lookup"><span data-stu-id="e3415-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="e3415-157">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-157">Obsolete.</span></span>   |
| [<span data-ttu-id="e3415-158">**думпмеморитраккер**</span><span class="sxs-lookup"><span data-stu-id="e3415-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="e3415-159">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e3415-159">Obsolete.</span></span>   |



 

 

 




