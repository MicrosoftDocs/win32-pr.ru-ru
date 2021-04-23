---
title: Cursor (Справочник по элементам пользовательского интерфейса MSAA)
description: Курсор представляет собой небольшое изображение, положение которого на экране управляется указывающим устройством, например мышью, пером или трекболом. Когда пользователь перемещает указывающее устройство, операционная система Windows перемещает курсор.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328851"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="44da2-104">Cursor (Справочник по элементам пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="44da2-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="44da2-105">В этом разделе описываются курсоры в целях справочника по элементам пользовательского интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="44da2-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="44da2-106">Использование курсоров в различных платформах пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="44da2-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="44da2-107">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="44da2-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="44da2-108">Курсор представляет собой небольшое изображение, положение которого на экране управляется указывающим устройством, например мышью, пером или трекболом.</span><span class="sxs-lookup"><span data-stu-id="44da2-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="44da2-109">Когда пользователь перемещает указывающее устройство, операционная система Windows перемещает курсор.</span><span class="sxs-lookup"><span data-stu-id="44da2-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="44da2-110">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="44da2-110">IAccessible Methods</span></span>

<span data-ttu-id="44da2-111">Курсор поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="44da2-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="44da2-112">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="44da2-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="44da2-113">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="44da2-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="44da2-114">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="44da2-114">IAccessible Properties</span></span>

<span data-ttu-id="44da2-115">Курсор поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="44da2-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="44da2-116">[**Get \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— свойство **ChildCount** равно нулю.</span><span class="sxs-lookup"><span data-stu-id="44da2-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="44da2-117">[**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— разработчики могут создавать пользовательские курсоры или использовать стандартные курсоры, ОПРЕДЕЛЯЕМые по идентификатору курсора.</span><span class="sxs-lookup"><span data-stu-id="44da2-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="44da2-118">Свойство **Name** курсора зависит от его формы и является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="44da2-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="44da2-119">Форма курсора</span><span class="sxs-lookup"><span data-stu-id="44da2-119">Cursor shape</span></span>     | <span data-ttu-id="44da2-120">Имя</span><span class="sxs-lookup"><span data-stu-id="44da2-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="44da2-121">Пользовательский курсор</span><span class="sxs-lookup"><span data-stu-id="44da2-121">Custom cursor</span></span>    | <span data-ttu-id="44da2-122">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="44da2-122">"Unknown"</span></span>         |
    | <span data-ttu-id="44da2-123">\_стрелка IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-123">IDC\_ARROW</span></span>       | <span data-ttu-id="44da2-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="44da2-124">"Normal"</span></span>          |
    | <span data-ttu-id="44da2-125">\_ИБЕАМ IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="44da2-126">Редактор</span><span class="sxs-lookup"><span data-stu-id="44da2-126">"Edit"</span></span>            |
    | <span data-ttu-id="44da2-127">\_Ожидание IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-127">IDC\_WAIT</span></span>        | <span data-ttu-id="44da2-128">Ожидания</span><span class="sxs-lookup"><span data-stu-id="44da2-128">"Wait"</span></span>            |
    | <span data-ttu-id="44da2-129">\_перекрестный IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-129">IDC\_CROSS</span></span>       | <span data-ttu-id="44da2-130">Графических</span><span class="sxs-lookup"><span data-stu-id="44da2-130">"Graphic"</span></span>         |
    | <span data-ttu-id="44da2-131">СТРЕЛКА для IDC \_</span><span class="sxs-lookup"><span data-stu-id="44da2-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="44da2-132">Крывающемся</span><span class="sxs-lookup"><span data-stu-id="44da2-132">"Up"</span></span>              |
    | <span data-ttu-id="44da2-133">\_СИЗЕНВСЕ IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="44da2-134">"НВСЕ size"</span><span class="sxs-lookup"><span data-stu-id="44da2-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="44da2-135">\_СИЗЕНЕСВ IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="44da2-136">"НЕСВ size"</span><span class="sxs-lookup"><span data-stu-id="44da2-136">"NESW size"</span></span>       |
    | <span data-ttu-id="44da2-137">\_СИЗЕВЕ IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="44da2-138">"Размер по горизонтали"</span><span class="sxs-lookup"><span data-stu-id="44da2-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="44da2-139">\_СИЗЕНС IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="44da2-140">"Размер по вертикали"</span><span class="sxs-lookup"><span data-stu-id="44da2-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="44da2-141">\_СИЗЕАЛЛ IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="44da2-142">Поместить</span><span class="sxs-lookup"><span data-stu-id="44da2-142">"Move"</span></span>            |
    | <span data-ttu-id="44da2-143">IDC \_ No</span><span class="sxs-lookup"><span data-stu-id="44da2-143">IDC\_NO</span></span>          | <span data-ttu-id="44da2-144">Запрещено</span><span class="sxs-lookup"><span data-stu-id="44da2-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="44da2-145">\_АППСТАРТИНГ IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="44da2-146">"Запуск приложения"</span><span class="sxs-lookup"><span data-stu-id="44da2-146">"App start"</span></span>       |
    | <span data-ttu-id="44da2-147">\_Справка по IDC</span><span class="sxs-lookup"><span data-stu-id="44da2-147">IDC\_HELP</span></span>        | <span data-ttu-id="44da2-148">Позволяют</span><span class="sxs-lookup"><span data-stu-id="44da2-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="44da2-149">[**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— свойство **Role** является [**\_ системным \_ курсором роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="44da2-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="44da2-150">[**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— свойство **State** является сочетанием одного или нескольких из следующих [значений](object-state-constants.md):</span><span class="sxs-lookup"><span data-stu-id="44da2-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="44da2-151">[**Состояние \_ Системная \_ невидимая**](object-state-constants.md) \| [ **\_ Система состояний \_ с плавающей запятой**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="44da2-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="44da2-152">Примечания</span><span class="sxs-lookup"><span data-stu-id="44da2-152">Notes</span></span>

-   <span data-ttu-id="44da2-153">В отличие от других элементов пользовательского интерфейса, объект Cursor не имеет связанного с ним маркера окна.</span><span class="sxs-lookup"><span data-stu-id="44da2-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="44da2-154">Чтобы получить доступ к объекту Cursor, клиенты должны задать [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и подождать, пока объект курсора не выдаст события.</span><span class="sxs-lookup"><span data-stu-id="44da2-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44da2-155">См. также</span><span class="sxs-lookup"><span data-stu-id="44da2-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44da2-156">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="44da2-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




