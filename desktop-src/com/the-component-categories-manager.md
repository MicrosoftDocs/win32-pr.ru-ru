---
title: Диспетчер категорий компонентов
description: Диспетчер категорий компонентов
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486772"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="80e79-103">Диспетчер категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="80e79-103">The Component Categories Manager</span></span>

<span data-ttu-id="80e79-104">Чтобы упростить обработку категорий компонентов и обеспечить согласованность реестра, система предоставляет диспетчер категорий компонентов, COM-объект с идентификатором CLSID \_ СТДКОМПОНЕНТКАТЕГОРИЕСМГР CLSID.</span><span class="sxs-lookup"><span data-stu-id="80e79-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="80e79-105">Этот COM-объект предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="80e79-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="80e79-106">**икатинформатион**</span><span class="sxs-lookup"><span data-stu-id="80e79-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="80e79-107">**икатрегистер**</span><span class="sxs-lookup"><span data-stu-id="80e79-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="80e79-108">[**Икатинформатион**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) предоставляет методы для получения сведений о категориях, реализованных или необходимых определенным классом, и предоставляет сведения о категориях, зарегистрированных на данном компьютере.</span><span class="sxs-lookup"><span data-stu-id="80e79-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="80e79-109">[**Икатрегистер**](/windows/desktop/api/ComCat/nn-comcat-icatregister) предоставляет методы для регистрации и отмены регистрации сведений о категориях компонентов в реестре.</span><span class="sxs-lookup"><span data-stu-id="80e79-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="80e79-110">К ним относятся понятные для человека имена категорий и категории, реализованные или необходимые для данного компонента или класса.</span><span class="sxs-lookup"><span data-stu-id="80e79-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80e79-111">См. также</span><span class="sxs-lookup"><span data-stu-id="80e79-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80e79-112">Связывание значков с категорией</span><span class="sxs-lookup"><span data-stu-id="80e79-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="80e79-113">Категоризация по возможностям компонентов</span><span class="sxs-lookup"><span data-stu-id="80e79-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="80e79-114">Категоризация по возможностям контейнеров</span><span class="sxs-lookup"><span data-stu-id="80e79-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="80e79-115">Классы и ассоциации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="80e79-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="80e79-116">Определение категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="80e79-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




