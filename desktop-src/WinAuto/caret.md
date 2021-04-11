---
title: Курсор (Справочник по элементам пользовательского интерфейса MSAA)
description: Курсор является мигающей линией, блоком или точечным рисунком в клиентской области окна или в элементе управления, который принимает ввод с клавиатуры.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "103890179"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="5b54e-103">Курсор (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="5b54e-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="5b54e-104">В этом разделе описываются символы крышки для Справочника по элементам пользовательского интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="5b54e-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="5b54e-105">Использование «крышки» в различных платформах пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="5b54e-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="5b54e-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="5b54e-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="5b54e-107">Курсор является мигающей линией, блоком или точечным рисунком в клиентской области окна или в элементе управления, который принимает ввод с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="5b54e-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="5b54e-108">Указывает место вставки текста или графики.</span><span class="sxs-lookup"><span data-stu-id="5b54e-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="5b54e-109">Так как только одно окно во времени имеет фокус клавиатуры, в системе имеется только один курсор.</span><span class="sxs-lookup"><span data-stu-id="5b54e-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="5b54e-110">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="5b54e-110">IAccessible Methods</span></span>

<span data-ttu-id="5b54e-111">Курсор поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="5b54e-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="5b54e-112">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="5b54e-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="5b54e-113">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="5b54e-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="5b54e-114">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="5b54e-114">IAccessible Properties</span></span>

<span data-ttu-id="5b54e-115">Курсор поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="5b54e-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b54e-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="5b54e-116">Property</span></span></th>
<th><span data-ttu-id="5b54e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b54e-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b54e-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="5b54e-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="5b54e-119">Свойство <strong>ChildCount</strong> равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5b54e-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b54e-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="5b54e-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="5b54e-121">Свойство <strong>Name</strong> имеет значение &quot; Edit &quot; .</span><span class="sxs-lookup"><span data-stu-id="5b54e-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b54e-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="5b54e-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="5b54e-123">Свойство <strong>Role</strong> имеет значение <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span><span class="sxs-lookup"><span data-stu-id="5b54e-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b54e-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="5b54e-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="5b54e-125">Свойства <strong>State</strong> могут иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5b54e-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="5b54e-126">Ноль, что означает, что курсор является видимым</span><span class="sxs-lookup"><span data-stu-id="5b54e-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="5b54e-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="5b54e-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="5b54e-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b54e-128">Notes</span></span>

-   <span data-ttu-id="5b54e-129">В отличие от других элементов пользовательского интерфейса, у объекта курсора нет связанного с ним обработчика окна.</span><span class="sxs-lookup"><span data-stu-id="5b54e-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="5b54e-130">Чтобы получить доступ к объекту курсора, клиенты должны задать [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и дождаться, пока объект курсора не выдаст события.</span><span class="sxs-lookup"><span data-stu-id="5b54e-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="5b54e-131">Объект курсора в элементе управления "форматированный текст", предоставляемый Riched20.dll (который используется в текстовых редакторах, таких как Microsoft WordPad в Windows 98), не отправляет никаких [виневентс](winevents-infrastructure.md) при изменении его позиции во время выбора текста.</span><span class="sxs-lookup"><span data-stu-id="5b54e-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="5b54e-132">Когда пользователь нажимает клавишу SHIFT и клавиши со стрелками для выбора текста, объект курсора не активирует [**\_ объект события \_ локатиончанже**](event-constants.md) WinEvent.</span><span class="sxs-lookup"><span data-stu-id="5b54e-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="5b54e-133">Аналогично, если выделение устанавливается программно с помощью многофункциональных сообщений редактирования, объект курсора не отправляет никаких событий для указания его новой позиции.</span><span class="sxs-lookup"><span data-stu-id="5b54e-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="5b54e-134">Все приложения, использующие Riched20.dll, представляют эту проблему.</span><span class="sxs-lookup"><span data-stu-id="5b54e-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="5b54e-135">Приложения, использующие более ранние версии элемента управления Rich Edit, правильно отправляют события на основе выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="5b54e-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b54e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5b54e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b54e-137">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="5b54e-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




