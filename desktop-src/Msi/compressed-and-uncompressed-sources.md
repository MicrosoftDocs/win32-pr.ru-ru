---
description: Авторы пакетов могут уменьшить размер пакетов установки путем сжатия исходных файлов и включения их в CAB-файлы. Исходный образ файла может быть сжат, несжатым или смесьом обоих типов.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Сжатые и несжатые источники
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991363"
---
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="d851e-104">Сжатые и несжатые источники</span><span class="sxs-lookup"><span data-stu-id="d851e-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="d851e-105">Авторы пакетов могут уменьшить размер пакетов установки путем сжатия исходных файлов и включения их в [CAB-файлы](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="d851e-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="d851e-106">Исходный образ файла может быть сжат, несжатым или смесьом обоих типов.</span><span class="sxs-lookup"><span data-stu-id="d851e-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="d851e-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Сжатые источники</span><span class="sxs-lookup"><span data-stu-id="d851e-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="d851e-108">Источник, состоящий из полностью сжатых файлов, должен включать бит сжатого флага в свойстве [**сводки слов**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="d851e-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="d851e-109">Сжатые исходные файлы должны храниться в CAB-файлах, расположенных в потоке данных в файле. msi, или в отдельном CAB-файле, расположенном в корне исходного дерева.</span><span class="sxs-lookup"><span data-stu-id="d851e-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="d851e-110">Все CAB в источнике должны быть перечислены в [таблице Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="d851e-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d851e-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Несжатые источники</span><span class="sxs-lookup"><span data-stu-id="d851e-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="d851e-112">Источник, полностью состоящий из исходных файлов без сжатия, должен опускать бит сжатого флага из свойства [**сводки слов**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="d851e-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="d851e-113">Все несжатые файлы в источнике должны существовать в исходном дереве, указанном в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="d851e-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d851e-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Смешанные источники</span><span class="sxs-lookup"><span data-stu-id="d851e-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="d851e-115">Чтобы смешать сжатые и несжатые исходные файлы в одном и том же пакете, Переопределите значение свойства « [**Сводка**](word-count-summary.md) по умолчанию», установив флаги битов Мсидбфилеаттрибутескомпрессед или мсидбфилеаттрибутеснонкомпрессед для определенных файлов.</span><span class="sxs-lookup"><span data-stu-id="d851e-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="d851e-116">Эти битовые флаги задаются в столбце Attributes [таблицы File](file-table.md) , если состояние сжатия файла не соответствует значению по умолчанию, заданному в свойстве [**Сводка по словам**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="d851e-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="d851e-117">Например, если в свойстве " [**Сводка слов**](word-count-summary.md) " указано значение бит сжатого флага, все файлы обрабатываются как сжатые в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="d851e-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="d851e-118">Все несжатые файлы в источнике должны включать Мсидбфилеаттрибутеснонкомпрессед в столбец Attributes [таблицы File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="d851e-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="d851e-119">Несжатые файлы должны находиться в корне исходного дерева.</span><span class="sxs-lookup"><span data-stu-id="d851e-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="d851e-120">Если для свойства " [**Сводка слов**](word-count-summary.md) " задан флаг несжатых файлов, файлы по умолчанию обрабатываются как несжатые, а все сжатые файлы должны включать мсидбфилеаттрибутескомпрессед в столбец Attributes таблицы File.</span><span class="sxs-lookup"><span data-stu-id="d851e-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="d851e-121">Все сжатые файлы должны храниться в CAB-файлах, расположенных в потоке данных в файле. msi, или в отдельном CAB-файле, расположенном в корне исходного дерева.</span><span class="sxs-lookup"><span data-stu-id="d851e-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="d851e-122">Дополнительные сведения см. [в разделе Использование ящиков и сжатых источников](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="d851e-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 



