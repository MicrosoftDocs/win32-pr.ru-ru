---
title: Копирование данных из одного файла в другой
description: Копирование данных из одного файла в другой
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- Windows Media Format SDK, копирование данных
- Расширенный системный формат (ASF), копирование данных
- ASF (Расширенный системный формат), копирование данных
- потоки, копирование данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986769"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="55376-107">Копирование данных из одного файла в другой</span><span class="sxs-lookup"><span data-stu-id="55376-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="55376-108">На самом базовом уровне копирование потока из одного файла ASF в другой довольно просто.</span><span class="sxs-lookup"><span data-stu-id="55376-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="55376-109">Однако существуют проблемы, которые следует учитывать при работе с потоками из нескольких входных файлов или при копировании потоков, которые были первоначально распакованы и повторно кодируются.</span><span class="sxs-lookup"><span data-stu-id="55376-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="55376-110">В следующих разделах описывается копирование потоков.</span><span class="sxs-lookup"><span data-stu-id="55376-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="55376-111">Section</span><span class="sxs-lookup"><span data-stu-id="55376-111">Section</span></span>                                                                                              | <span data-ttu-id="55376-112">дескрипитон</span><span class="sxs-lookup"><span data-stu-id="55376-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55376-113">Копирование потоков без распаковки данных</span><span class="sxs-lookup"><span data-stu-id="55376-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="55376-114">Описывает копирование потоков с помощью сжатых образцов для сохранения качества содержимого.</span><span class="sxs-lookup"><span data-stu-id="55376-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="55376-115">Копирование потоков с использованием распакованных образцов</span><span class="sxs-lookup"><span data-stu-id="55376-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="55376-116">Описывает проблемы при копировании потоков с помощью распакованных образцов.</span><span class="sxs-lookup"><span data-stu-id="55376-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="55376-117">См. также</span><span class="sxs-lookup"><span data-stu-id="55376-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55376-118">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="55376-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="55376-119">**Объект конфигурации потока**</span><span class="sxs-lookup"><span data-stu-id="55376-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="55376-120">**Объект модуля синхронного чтения**</span><span class="sxs-lookup"><span data-stu-id="55376-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="55376-121">**Объект модуля записи**</span><span class="sxs-lookup"><span data-stu-id="55376-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




