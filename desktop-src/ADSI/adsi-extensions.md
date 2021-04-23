---
title: Расширения ADSI
description: Расширение ADSI — это специальный COM-объект, позволяющий разработчику расширить объект ADSI.
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- Расширения ADSI
- ADSI ADSI, использование расширений
- расширения ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067339"
---
# <a name="adsi-extensions"></a><span data-ttu-id="a3acf-106">Расширения ADSI</span><span class="sxs-lookup"><span data-stu-id="a3acf-106">ADSI Extensions</span></span>

<span data-ttu-id="a3acf-107">Расширение ADSI — это специальный COM-объект, позволяющий разработчику расширить объект ADSI.</span><span class="sxs-lookup"><span data-stu-id="a3acf-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="a3acf-108">Каждое расширение связано с указанным классом в каталоге.</span><span class="sxs-lookup"><span data-stu-id="a3acf-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="a3acf-109">С помощью этой модели расширения разработчики могут добавлять методы, чтобы дать объекту более динамичное значение.</span><span class="sxs-lookup"><span data-stu-id="a3acf-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="a3acf-110">В традиционной модели программирования каталога доступ к объекту осуществляется путем получения и задания атрибутов объекта.</span><span class="sxs-lookup"><span data-stu-id="a3acf-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="a3acf-111">С помощью расширений ADSI можно добавить дополнительные компоненты в объект каталога.</span><span class="sxs-lookup"><span data-stu-id="a3acf-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="a3acf-112">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="a3acf-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="a3acf-113">Преимущества использования расширений ADSI</span><span class="sxs-lookup"><span data-stu-id="a3acf-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="a3acf-114">Архитектура расширения ADSI</span><span class="sxs-lookup"><span data-stu-id="a3acf-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="a3acf-115">Интеграция расширений в ADSI</span><span class="sxs-lookup"><span data-stu-id="a3acf-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="a3acf-116">Что видят клиенты?</span><span class="sxs-lookup"><span data-stu-id="a3acf-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="a3acf-117">Получение интерфейсов ADSI из расширения</span><span class="sxs-lookup"><span data-stu-id="a3acf-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="a3acf-118">Библиотеки типов расширений ADSI</span><span class="sxs-lookup"><span data-stu-id="a3acf-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="a3acf-119">Поддержка раннего связывания</span><span class="sxs-lookup"><span data-stu-id="a3acf-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="a3acf-120">Поддержка поздних привязок</span><span class="sxs-lookup"><span data-stu-id="a3acf-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="a3acf-121">Интерфейс Иадсекстенсион</span><span class="sxs-lookup"><span data-stu-id="a3acf-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="a3acf-122">Поддержка сдвоенных или интерфейсов диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="a3acf-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="a3acf-123">Повторное посещение правил агрегирования COM с помощью расширений ADSI</span><span class="sxs-lookup"><span data-stu-id="a3acf-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="a3acf-124">Разрешение нескольких компонентов статистической обработки, поддерживающих один и тот же интерфейс</span><span class="sxs-lookup"><span data-stu-id="a3acf-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="a3acf-125">Разрешение конфликтов имен функций и свойств в автоматизации в расширениях</span><span class="sxs-lookup"><span data-stu-id="a3acf-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




