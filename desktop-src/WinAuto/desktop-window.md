---
title: Окно рабочего стола (Справочник по элементам пользовательского интерфейса MSAA)
description: В окне рабочего стола отображается представление списка рабочего стола (в котором содержатся значки, такие как Мой компьютер) и панель задач, содержащая кнопку «Пуск».
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410704"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="cee9f-103">Окно рабочего стола (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="cee9f-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="cee9f-104">В окне рабочего стола отображается представление списка рабочего стола (в котором содержатся значки, такие как Мой компьютер) и панель задач, содержащая кнопку « **Пуск** ».</span><span class="sxs-lookup"><span data-stu-id="cee9f-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="cee9f-105">Этот объект редко запрашивается клиентами, так как представление списка и панель задач охватывают весь рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="cee9f-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="cee9f-106">Объект Desktop извлекается при входе в систему, прежде чем оболочка операционной системы отобразит представление списка и панель задач.</span><span class="sxs-lookup"><span data-stu-id="cee9f-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="cee9f-107">В некоторых случаях Рабочий стол получается при переходе от других объектов.</span><span class="sxs-lookup"><span data-stu-id="cee9f-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="cee9f-108">Имя класса Window для окна рабочего стола — " \# 32769".</span><span class="sxs-lookup"><span data-stu-id="cee9f-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="cee9f-109">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="cee9f-109">IAccessible Methods</span></span>

<span data-ttu-id="cee9f-110">Окно рабочего стола поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="cee9f-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="cee9f-111">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="cee9f-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="cee9f-112">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="cee9f-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="cee9f-113">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="cee9f-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="cee9f-114">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="cee9f-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="cee9f-115">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="cee9f-115">IAccessible Properties</span></span>

<span data-ttu-id="cee9f-116">Окно рабочего стола поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="cee9f-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="cee9f-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="cee9f-117">Property</span></span>                                                                 | <span data-ttu-id="cee9f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cee9f-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cee9f-119">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="cee9f-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="cee9f-120">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="cee9f-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="cee9f-121">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="cee9f-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="cee9f-122">Свойство Name имеет значение "Desktop".</span><span class="sxs-lookup"><span data-stu-id="cee9f-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="cee9f-123">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="cee9f-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="cee9f-124">Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cee9f-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="cee9f-125">**получить \_ аккселектион**</span><span class="sxs-lookup"><span data-stu-id="cee9f-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="cee9f-126">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="cee9f-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="cee9f-127">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md):[**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="cee9f-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="cee9f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cee9f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee9f-129">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="cee9f-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





