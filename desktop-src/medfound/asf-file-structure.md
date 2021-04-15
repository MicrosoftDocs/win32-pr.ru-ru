---
description: В этом разделе описывается структура файла в формате ASF.
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Структура файла ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539656"
---
# <a name="asf-file-structure"></a><span data-ttu-id="786b8-103">Структура файла ASF</span><span class="sxs-lookup"><span data-stu-id="786b8-103">ASF File Structure</span></span>

<span data-ttu-id="786b8-104">В этом разделе описывается структура файла в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="786b8-105">Чтобы получить подробные сведения о файлах ASF, скачайте [спецификацию ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="786b8-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="786b8-106">Вы также можете использовать средство [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) для просмотра структуры существующего файла ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="786b8-107">Базовая единица Организации для файлов ASF называется *объектом*.</span><span class="sxs-lookup"><span data-stu-id="786b8-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="786b8-108">Объект файла ASF содержит следующие данные.</span><span class="sxs-lookup"><span data-stu-id="786b8-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="786b8-109">Данные</span><span class="sxs-lookup"><span data-stu-id="786b8-109">Data</span></span>                                                        | <span data-ttu-id="786b8-110">Размер</span><span class="sxs-lookup"><span data-stu-id="786b8-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="786b8-111">Идентификатор GUID, определяющий объект.</span><span class="sxs-lookup"><span data-stu-id="786b8-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="786b8-112">128 бит</span><span class="sxs-lookup"><span data-stu-id="786b8-112">128 bits</span></span> |
| <span data-ttu-id="786b8-113">Размер объекта.</span><span class="sxs-lookup"><span data-stu-id="786b8-113">The size of the object.</span></span>                                     | <span data-ttu-id="786b8-114">64 — бит.</span><span class="sxs-lookup"><span data-stu-id="786b8-114">64-bits.</span></span> |
| <span data-ttu-id="786b8-115">Данные объекта.</span><span class="sxs-lookup"><span data-stu-id="786b8-115">Object data.</span></span> <span data-ttu-id="786b8-116">Данные объекта могут содержать другие объекты ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="786b8-117">Возможны разные варианты.</span><span class="sxs-lookup"><span data-stu-id="786b8-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="786b8-118">Объект ASF-файла — это просто фрагмент данных.</span><span class="sxs-lookup"><span data-stu-id="786b8-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="786b8-119">Это не объект в смысле программирования на компьютере.</span><span class="sxs-lookup"><span data-stu-id="786b8-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="786b8-120">Файл ASF содержит три типа файловых объектов верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="786b8-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="786b8-121">Файл ASF</span><span class="sxs-lookup"><span data-stu-id="786b8-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="786b8-122">Описание</span><span class="sxs-lookup"><span data-stu-id="786b8-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="786b8-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Объект Header</span><span class="sxs-lookup"><span data-stu-id="786b8-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="786b8-124">Содержит сведения о файле ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="786b8-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Объект данных</span><span class="sxs-lookup"><span data-stu-id="786b8-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="786b8-126">Содержит пакеты данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="786b8-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="786b8-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Объекты индекса</span><span class="sxs-lookup"><span data-stu-id="786b8-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="786b8-128">Содержит один или несколько индексов.</span><span class="sxs-lookup"><span data-stu-id="786b8-128">Contains one or more indexes.</span></span> <span data-ttu-id="786b8-129">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="786b8-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="786b8-130">На следующей схеме показана структура файла ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-130">The following diagram shows the ASF file structure.</span></span>

![Схема, показывающая структуру файлов ASF, включая элементы в заголовке, данных и индексе](images/asf-components04.png)

<span data-ttu-id="786b8-132">Диаграмма не рисуется для масштабирования; обычно объект данных состоит из большей части файла.</span><span class="sxs-lookup"><span data-stu-id="786b8-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="786b8-133">Объект Header</span><span class="sxs-lookup"><span data-stu-id="786b8-133">Header Object</span></span>

<span data-ttu-id="786b8-134">Объект заголовка является обязательным и отображается в начале каждого ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="786b8-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="786b8-135">Он содержит глобальные атрибуты файлов и сведения о потоках в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="786b8-136">Эти сведения используются для интерпретации и воспроизведения данных в файле.</span><span class="sxs-lookup"><span data-stu-id="786b8-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="786b8-137">Объект заголовка содержит несколько подобъектов мадатори:</span><span class="sxs-lookup"><span data-stu-id="786b8-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="786b8-138">Объект свойств файла описывает глобальные атрибуты файла, например размер файла, длительность воспроизведения, число пакетов данных, минимальный и максимальный размер пакета и максимальную скорость.</span><span class="sxs-lookup"><span data-stu-id="786b8-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="786b8-139">Объект расширения заголовка позволяет добавлять дополнительные функции в файл ASF, сохраняя при этом обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="786b8-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="786b8-140">Объект свойств потока описывает один поток в файле.</span><span class="sxs-lookup"><span data-stu-id="786b8-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="786b8-141">Файл ASF должен содержать по крайней мере один поток, поэтому по крайней мере один объект свойств потока.</span><span class="sxs-lookup"><span data-stu-id="786b8-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="786b8-142">Объект заголовка может содержать дополнительные дополнительные сведения, включая метаданные о файле (например, заголовок и автора), список кодеков, используемых для кодирования файла, и сведения о защите содержимого.</span><span class="sxs-lookup"><span data-stu-id="786b8-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="786b8-143">Объект данных</span><span class="sxs-lookup"><span data-stu-id="786b8-143">Data Object</span></span>

<span data-ttu-id="786b8-144">Объект данных ASF содержит все данные мультимедиа для файла ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="786b8-145">Этот объект является обязательным и должен следовать за объектом заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="786b8-146">Объект данных делится на *пакеты* данных.</span><span class="sxs-lookup"><span data-stu-id="786b8-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="786b8-147">Каждый пакет содержит данные для одного или нескольких потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="786b8-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="786b8-148">Пакет данных содержит заголовок пакета данных, который предоставляет сведения о синтаксическом анализе пакетов, а также полезные данные для фактических данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="786b8-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="786b8-149">Со всеми пакетами данных связано время презентации и они упорядочиваются в полученном порядке.</span><span class="sxs-lookup"><span data-stu-id="786b8-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="786b8-150">Сведения о содержимом объекта данных, например размер пакета и число пакетов, хранятся в объекте заголовка.</span><span class="sxs-lookup"><span data-stu-id="786b8-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="786b8-151">Объект index</span><span class="sxs-lookup"><span data-stu-id="786b8-151">Index Object</span></span>

<span data-ttu-id="786b8-152">Объект index является необязательным и является последним объектом в ASF-файле.</span><span class="sxs-lookup"><span data-stu-id="786b8-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="786b8-153">Файл ASF может содержать более одного объекта индекса.</span><span class="sxs-lookup"><span data-stu-id="786b8-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="786b8-154">Объект index обеспечивает произвольный доступ на основе времени к объекту данных ASF.</span><span class="sxs-lookup"><span data-stu-id="786b8-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="786b8-155">Простой объект индекса — это еще один тип индекса.</span><span class="sxs-lookup"><span data-stu-id="786b8-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="786b8-156">См. также</span><span class="sxs-lookup"><span data-stu-id="786b8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="786b8-157">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="786b8-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




