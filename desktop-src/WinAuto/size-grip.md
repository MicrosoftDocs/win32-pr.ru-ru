---
title: Захват размера (Справочник по элементам пользовательского интерфейса MSAA)
description: Захват размера — это Специальный указатель мыши в правом нижнем углу окна, который позволяет пользователю щелкнуть и перетащить захват размера, чтобы изменить размер окна.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779670"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="469bc-103">Захват размера (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="469bc-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="469bc-104">Захват размера — это Специальный указатель мыши в правом нижнем углу окна, который позволяет пользователю щелкнуть и перетащить захват размера, чтобы изменить размер окна.</span><span class="sxs-lookup"><span data-stu-id="469bc-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="469bc-105">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="469bc-105">IAccessible Methods</span></span>

<span data-ttu-id="469bc-106">Захват размера поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="469bc-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="469bc-107">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="469bc-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="469bc-108">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="469bc-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="469bc-109">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="469bc-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="469bc-110">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="469bc-110">IAccessible Properties</span></span>

<span data-ttu-id="469bc-111">Захват размера поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="469bc-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="469bc-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="469bc-112">Property</span></span>                                                                   | <span data-ttu-id="469bc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="469bc-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="469bc-114">**получить \_ аккдескриптион**</span><span class="sxs-lookup"><span data-stu-id="469bc-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="469bc-115">Свойство **Description** — может использоваться для изменения ширины и высоты окна.</span><span class="sxs-lookup"><span data-stu-id="469bc-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="469bc-116">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="469bc-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="469bc-117">Свойство **Name** имеет значение "поле size".</span><span class="sxs-lookup"><span data-stu-id="469bc-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="469bc-118">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="469bc-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="469bc-119">Окно, содержащее захват размера.</span><span class="sxs-lookup"><span data-stu-id="469bc-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="469bc-120">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="469bc-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="469bc-121">Свойство **Role** — [**\_ \_ захват системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="469bc-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="469bc-122">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="469bc-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="469bc-123">Значение свойства **State** равно нулю, что означает, что объект является видимым, или [**Система состояний \_ \_ невидима**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="469bc-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="469bc-124">См. также</span><span class="sxs-lookup"><span data-stu-id="469bc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="469bc-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="469bc-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




