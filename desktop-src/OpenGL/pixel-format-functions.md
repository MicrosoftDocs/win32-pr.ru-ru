---
title: Функции формата пикселей
description: Следующие функции Windows управляют форматами пикселей.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Функции ВГЛ, формат пикселей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889120"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="5de8f-104">Функции формата пикселей</span><span class="sxs-lookup"><span data-stu-id="5de8f-104">Pixel Format Functions</span></span>

<span data-ttu-id="5de8f-105">Следующие функции Windows управляют форматами пикселей.</span><span class="sxs-lookup"><span data-stu-id="5de8f-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="5de8f-106">Функция Windows</span><span class="sxs-lookup"><span data-stu-id="5de8f-106">Windows Function</span></span>                                               | <span data-ttu-id="5de8f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5de8f-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5de8f-108">**чусепикселформат**</span><span class="sxs-lookup"><span data-stu-id="5de8f-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="5de8f-109">Получает формат пикселей контекста устройства, который наиболее близко соответствует указанному формату пикселей.</span><span class="sxs-lookup"><span data-stu-id="5de8f-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="5de8f-110">**сетпикселформат**</span><span class="sxs-lookup"><span data-stu-id="5de8f-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="5de8f-111">Задает текущий формат пикселей контекста устройства в формате пикселей, заданном индексом формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="5de8f-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="5de8f-112">**жетпикселформат**</span><span class="sxs-lookup"><span data-stu-id="5de8f-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="5de8f-113">Получает индекс формата пикселей текущего формата пикселей контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="5de8f-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="5de8f-114">**дескрибепикселформат**</span><span class="sxs-lookup"><span data-stu-id="5de8f-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="5de8f-115">При наличии контекста устройства и индекса формата пикселей заполняет структуру данных [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) свойствами формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="5de8f-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="5de8f-116">**жетенхметафилепикселформат**</span><span class="sxs-lookup"><span data-stu-id="5de8f-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="5de8f-117">Извлекает сведения о формате пикселей для расширенного метафайла.</span><span class="sxs-lookup"><span data-stu-id="5de8f-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="5de8f-118">Функция [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) возвращает индекс формата пикселей, основанный на единицах, который определяет наилучшее соответствие из поддерживаемых форматов пикселей контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="5de8f-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="5de8f-119">Функция [**сетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) определяет нужный формат, используя индекс формата пикселей с одним исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="5de8f-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="5de8f-120">Как правило, вызывается **чусепикселформат** для поиска наиболее подходящего формата пикселей, а затем вызывается **Сетпикселформат** с результатом **чусепикселформат**.</span><span class="sxs-lookup"><span data-stu-id="5de8f-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="5de8f-121">При вызове **сетпикселформат** для контекста устройства, который ссылается на окно, **сетпикселформат** также изменяет формат пикселей окна.</span><span class="sxs-lookup"><span data-stu-id="5de8f-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="5de8f-122">Установка формата пикселей окна более одного раза может привести к значительным осложнениям диспетчера окон и многопоточных приложений, поэтому это недопустимо.</span><span class="sxs-lookup"><span data-stu-id="5de8f-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="5de8f-123">Формат пикселей окна можно задать только один раз. После этого формат пикселей окна изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="5de8f-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="5de8f-124">Функция [**жетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) возвращает индекс формата пикселей, основанный на одном элементе.</span><span class="sxs-lookup"><span data-stu-id="5de8f-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="5de8f-125">Функция [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) принимает в качестве параметров следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5de8f-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="5de8f-126">Маркер контекста устройства</span><span class="sxs-lookup"><span data-stu-id="5de8f-126">A handle to a device context</span></span>
-   <span data-ttu-id="5de8f-127">Индекс формата пикселей</span><span class="sxs-lookup"><span data-stu-id="5de8f-127">A pixel format index</span></span>
-   <span data-ttu-id="5de8f-128">Указатель на структуру данных [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)</span><span class="sxs-lookup"><span data-stu-id="5de8f-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="5de8f-129">Функция [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) возвращает с элементами **пикселформатдескриптор** , соответствующим образом установленным.</span><span class="sxs-lookup"><span data-stu-id="5de8f-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="5de8f-130">Функция **жетенхметафилепикселформат** возвращает размер формата пикселей метафайла и получает сведения о формате пикселей метафайла.</span><span class="sxs-lookup"><span data-stu-id="5de8f-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




