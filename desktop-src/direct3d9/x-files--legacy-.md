---
description: Формат файла X относится к файлам с расширением имени файла. x.
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: X-файлы (прежние версии) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894302"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="1e7de-103">X-файлы (прежние версии) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e7de-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="1e7de-104">Формат файла X относится к файлам с расширением имени файла. x.</span><span class="sxs-lookup"><span data-stu-id="1e7de-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="1e7de-105">Файлы X были введены в DirectX 2,0.</span><span class="sxs-lookup"><span data-stu-id="1e7de-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="1e7de-106">Двоичная версия этого формата была впоследствии выпущена с помощью DirectX 3,0, которая также описана в этой документации.</span><span class="sxs-lookup"><span data-stu-id="1e7de-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="1e7de-107">В DirectX 6,0 появились интерфейсы и методы, обеспечивающие чтение и запись в файлы. x.</span><span class="sxs-lookup"><span data-stu-id="1e7de-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="1e7de-108">X-файлы предоставляют формат, основанный на шаблонах, который позволяет хранить сетки, текстуры, анимации и определяемые пользователем объекты.</span><span class="sxs-lookup"><span data-stu-id="1e7de-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="1e7de-109">Поддержка наборов анимации позволяет хранить предопределенные пути для воспроизведения в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="1e7de-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="1e7de-110">Также поддерживаются создание экземпляров и иерархий.</span><span class="sxs-lookup"><span data-stu-id="1e7de-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="1e7de-111">Создание экземпляров позволяет создавать несколько ссылок на объект, например в сетку, сохраняя данные только один раз для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="1e7de-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="1e7de-112">Иерархии используются для выражения связей между записями данных.</span><span class="sxs-lookup"><span data-stu-id="1e7de-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="1e7de-113">Формат файла. x предоставляет примитивы данных низкого уровня, на которых приложения определяют примитивы более высокого уровня через шаблоны.</span><span class="sxs-lookup"><span data-stu-id="1e7de-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="1e7de-114">Трехмерные модели, созданные в приложениях скрытые 3ds Max или alias \| файл Wavefront Maya, можно преобразовать в файлы. x с помощью расширений DirectX для псевдонима Maya.</span><span class="sxs-lookup"><span data-stu-id="1e7de-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="1e7de-115">В этом разделе описывается структура файлов. x и способы их использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="1e7de-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="1e7de-116">Сведения делятся на следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="1e7de-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="1e7de-117">Загрузка файла X (прежних версий) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e7de-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="1e7de-118">Сохранение в файл X (прежний) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e7de-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="1e7de-119">Определение простого куба (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e7de-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="1e7de-120">Добавление текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e7de-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="1e7de-121">Добавление кадров и анимации (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e7de-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="1e7de-122">Дополнительные сведения о формате x см. в разделе Справочник по [x File](dx9-graphics-reference-d3dx-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="1e7de-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="1e7de-123">Дополнительные сведения об API-файле x см. в разделе [Справочник по файлам x (прежние версии)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="1e7de-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e7de-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1e7de-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e7de-125">Начало работы</span><span class="sxs-lookup"><span data-stu-id="1e7de-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



