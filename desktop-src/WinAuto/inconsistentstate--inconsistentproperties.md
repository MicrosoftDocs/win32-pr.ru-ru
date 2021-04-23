---
title: Инконсистентстате, Инконсистентпропертиес
description: Инконсистентстате, Инконсистентпропертиес
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774264"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="d6b13-103">Инконсистентстате, Инконсистентпропертиес</span><span class="sxs-lookup"><span data-stu-id="d6b13-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="d6b13-104">Текст</span><span class="sxs-lookup"><span data-stu-id="d6b13-104">Text</span></span>

<span data-ttu-id="d6b13-105">Элемент управления имеет несоответствующие {0} состояния или свойства. {1}</span><span class="sxs-lookup"><span data-stu-id="d6b13-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="d6b13-106">Тип</span><span class="sxs-lookup"><span data-stu-id="d6b13-106">Type</span></span>

<span data-ttu-id="d6b13-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d6b13-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="d6b13-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d6b13-108">Description</span></span>

<span data-ttu-id="d6b13-109">Элемент сообщает о несоответствиях или конфликтующих состояниях MSAA или свойств модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d6b13-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="d6b13-110">Например, если метод [**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) возвращает любое из следующих сочетаний.</span><span class="sxs-lookup"><span data-stu-id="d6b13-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="d6b13-111">\_Развернутая система состояний \_ и \_ Система состояний \_ свернуты</span><span class="sxs-lookup"><span data-stu-id="d6b13-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="d6b13-112">\_Система состояний \_ выбрана и не является выбранной \_ системой состояния \_</span><span class="sxs-lookup"><span data-stu-id="d6b13-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="d6b13-113">Система \_ состояний \_ с \_ фокусом и без системы состояний \_</span><span class="sxs-lookup"><span data-stu-id="d6b13-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="d6b13-114">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку пользователь может сообщить о неправильном состоянии элемента.</span><span class="sxs-lookup"><span data-stu-id="d6b13-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d6b13-115">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="d6b13-115">Possible causes</span></span>

<span data-ttu-id="d6b13-116">Для элемента или его родителя задано неправильное состояние MSAA.</span><span class="sxs-lookup"><span data-stu-id="d6b13-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6b13-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d6b13-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6b13-118">**IAccessible:: Get \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="d6b13-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="d6b13-119">**Константы состояния объектов**</span><span class="sxs-lookup"><span data-stu-id="d6b13-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="d6b13-120">Состояния и свойства</span><span class="sxs-lookup"><span data-stu-id="d6b13-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




