---
title: Статический текст (Справочник по элементам пользовательского интерфейса MSAA)
description: Элементы управления "статический текст" предоставляют удобный способ для вывода текста в диалоговых окнах и других окнах. Статические текстовые элементы управления часто служат метками для других элементов управления.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889095"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="1d4f1-104">Статический текст (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="1d4f1-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="1d4f1-105">Элементы управления "статический текст" предоставляют удобный способ для вывода текста в диалоговых окнах и других окнах.</span><span class="sxs-lookup"><span data-stu-id="1d4f1-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="1d4f1-106">Статические текстовые элементы управления часто служат метками для других элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1d4f1-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="1d4f1-107">Имя класса окна для статического текстового элемента управления — «STATIC».</span><span class="sxs-lookup"><span data-stu-id="1d4f1-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="1d4f1-108">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d4f1-108">IAccessible Methods</span></span>

<span data-ttu-id="1d4f1-109">Элементы управления "статический текст" поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1d4f1-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="1d4f1-110">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="1d4f1-111">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="1d4f1-112">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="1d4f1-113">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="1d4f1-114">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d4f1-114">IAccessible Properties</span></span>

<span data-ttu-id="1d4f1-115">Элементы управления "статический текст" поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1d4f1-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="1d4f1-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="1d4f1-116">Property</span></span>                                                                             | <span data-ttu-id="1d4f1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d4f1-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d4f1-118">**получить \_ аккчилд**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d4f1-119">**получить \_ аккчилдкаунт**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="1d4f1-120">Свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1d4f1-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1d4f1-121">**получить \_ аккдескриптион**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d4f1-122">**получить \_ аккфокус**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d4f1-123">**получить \_ акчелп**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d4f1-124">**получить \_ акчелптопик**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d4f1-125">**получить \_ акккэйбоардшорткут**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="1d4f1-126">Свойство **кэйбоардшорткут** — это клавиша доступа, которая является подчеркнутым символом в тексте, который активирует элемент управления, связанный со статическим текстом.</span><span class="sxs-lookup"><span data-stu-id="1d4f1-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="1d4f1-127">Возвращаемая строка содержит символ клавиши доступа, добавленный к строке "Alt +".</span><span class="sxs-lookup"><span data-stu-id="1d4f1-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="1d4f1-128">**получить \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="1d4f1-129">Свойство **Name** совпадает с текстом в элементе управления "статический текст".</span><span class="sxs-lookup"><span data-stu-id="1d4f1-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="1d4f1-130">**получить \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="1d4f1-131">**Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.</span><span class="sxs-lookup"><span data-stu-id="1d4f1-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="1d4f1-132">**получить \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="1d4f1-133">Свойство **Role** имеет [**роль \_ System \_ статиктекст**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1d4f1-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="1d4f1-134">**получить \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="1d4f1-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="1d4f1-135">Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): системная система состояний с состоянием " [**\_ \_ только для чтения**](object-state-constants.md) " \| [**\_ \_ невидима**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1d4f1-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="1d4f1-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d4f1-136">Notes</span></span>

-   <span data-ttu-id="1d4f1-137">Метод [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) Возвращает отображаемое значение \_ E \_ мембернотфаунд при вызове с помощью [**селфлаг \_ такефокус**](selflag.md) для статического текстового объекта.</span><span class="sxs-lookup"><span data-stu-id="1d4f1-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="1d4f1-138">Статические элементы управления с \_ стилем значка SS возвращают недопустимые данные в свойстве **Name** .</span><span class="sxs-lookup"><span data-stu-id="1d4f1-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d4f1-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1d4f1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d4f1-140">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d4f1-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





