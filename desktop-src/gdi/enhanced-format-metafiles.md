---
description: Enhanced-Format метафайлы
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Enhanced-Format метафайлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984973"
---
# <a name="enhanced-format-metafiles"></a><span data-ttu-id="884b4-103">Enhanced-Format метафайлы</span><span class="sxs-lookup"><span data-stu-id="884b4-103">Enhanced-Format Metafiles</span></span>

<span data-ttu-id="884b4-104">*Метафайл расширенного формата* состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="884b4-104">The *enhanced-format metafile* consists of the following elements:</span></span>

-   <span data-ttu-id="884b4-105">Заголовок</span><span class="sxs-lookup"><span data-stu-id="884b4-105">A header</span></span>
-   <span data-ttu-id="884b4-106">Таблица дескрипторов объектов GDI</span><span class="sxs-lookup"><span data-stu-id="884b4-106">A table of handles to GDI objects</span></span>
-   <span data-ttu-id="884b4-107">Частная палитра</span><span class="sxs-lookup"><span data-stu-id="884b4-107">A private palette</span></span>
-   <span data-ttu-id="884b4-108">Массив записей метафайлов</span><span class="sxs-lookup"><span data-stu-id="884b4-108">An array of metafile records</span></span>

<span data-ttu-id="884b4-109">Расширенные метафайлы обеспечивают истинную независимость от устройств.</span><span class="sxs-lookup"><span data-stu-id="884b4-109">Enhanced metafiles provide true device independence.</span></span> <span data-ttu-id="884b4-110">Изображение, хранящееся в расширенном метафайле, можно представить в виде моментального снимка видеоролика, созданной в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="884b4-110">You can think of the picture stored in an enhanced metafile as a "snapshot" of the video display taken at a particular moment.</span></span> <span data-ttu-id="884b4-111">Этот "моментальный снимок" сохраняет свои размеры независимо от того, где он отображается на принтере, на плоттере, на рабочем столе или в клиентской области любого приложения.</span><span class="sxs-lookup"><span data-stu-id="884b4-111">This "snapshot" maintains its dimensions no matter where it appears on a printer, a plotter, the desktop, or in the client area of any application.</span></span>

<span data-ttu-id="884b4-112">Можно использовать расширенные метафайлы для хранения изображений, созданных с помощью функций GDI (включая новые функции PATH и преобразования).</span><span class="sxs-lookup"><span data-stu-id="884b4-112">You can use enhanced metafiles to store a picture created by using the GDI functions (including new path and transformation functions).</span></span> <span data-ttu-id="884b4-113">Поскольку формат расширенного метафайла является стандартизированным, рисунки, хранящиеся в этом формате, можно копировать из одного приложения в другое. и, так как изображения действительно независимы от устройства, они гарантированно сохраняют свою форму и пропорции на любом устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="884b4-113">Because the enhanced metafile format is standardized, pictures that are stored in this format can be copied from one application to another; and, because the pictures are truly device independent, they are guaranteed to maintain their shape and proportion on any output device.</span></span>

-   [<span data-ttu-id="884b4-114">Расширенные записи метафайлов</span><span class="sxs-lookup"><span data-stu-id="884b4-114">Enhanced Metafile Records</span></span>](enhanced-metafile-records.md)
-   [<span data-ttu-id="884b4-115">Расширенное создание метафайлов</span><span class="sxs-lookup"><span data-stu-id="884b4-115">Enhanced Metafile Creation</span></span>](enhanced-metafile-creation.md)
-   [<span data-ttu-id="884b4-116">Операции расширенного метафайла</span><span class="sxs-lookup"><span data-stu-id="884b4-116">Enhanced Metafile Operations</span></span>](enhanced-metafile-operations.md)

 

 



