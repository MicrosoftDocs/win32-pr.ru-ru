---
title: Создание мастеров
description: Мастер — это тип страницы свойств, предоставляющий простой и эффективный способ указания пользователей в процедуре.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105656829"
---
# <a name="how-to-create-wizards"></a><span data-ttu-id="1c733-103">Создание мастеров</span><span class="sxs-lookup"><span data-stu-id="1c733-103">How to Create Wizards</span></span>

<span data-ttu-id="1c733-104">Мастер — это тип страницы свойств, предоставляющий простой и эффективный способ указания пользователей в процедуре.</span><span class="sxs-lookup"><span data-stu-id="1c733-104">A wizard is a type of property sheet that provides a simple and powerful way to guide users through a procedure.</span></span>

<span data-ttu-id="1c733-105">Мастера — это один из ключевых клавиш для упрощения взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="1c733-105">Wizards are one of the keys to simplifying the user experience.</span></span> <span data-ttu-id="1c733-106">Они позволяют выполнять сложные операции, такие как Настройка приложения, и разбивать их на несколько простых шагов.</span><span class="sxs-lookup"><span data-stu-id="1c733-106">They allow you to take a complex operation, such as configuration of an application, and break it into a series of simple steps.</span></span> <span data-ttu-id="1c733-107">В каждой точке процесса можно указать, что требуется, и отобразить элементы управления, позволяющие пользователю выбирать и вводить текст.</span><span class="sxs-lookup"><span data-stu-id="1c733-107">At each point in the process, you can provide an explanation of what is needed, and display controls that allow the user to make selections and enter text.</span></span>

<span data-ttu-id="1c733-108">На самом деле, мастер представляет собой тип страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-108">A wizard is actually a type of property sheet.</span></span> <span data-ttu-id="1c733-109">Страница свойств, по сути, является контейнером для коллекции *страниц*, где каждая страница является отдельным диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="1c733-109">A property sheet is essentially a container for a collection of *pages*, where each page is a separate dialog box.</span></span> <span data-ttu-id="1c733-110">В то время как обычные страницы свойств позволяют пользователю получить доступ к любой странице в любое время, мастера поочередно выдаются.</span><span class="sxs-lookup"><span data-stu-id="1c733-110">Whereas regular property sheets allow the user to access any page at any time, wizards present pages in sequence.</span></span> <span data-ttu-id="1c733-111">Вместо вкладок для перехода вперед и назад используются кнопки.</span><span class="sxs-lookup"><span data-stu-id="1c733-111">Instead of tabs, buttons are used to navigate forward and backward.</span></span> <span data-ttu-id="1c733-112">Порядок, в котором отображаются страницы, управляется приложением и может быть изменен в зависимости от введенных пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="1c733-112">The order in which pages are displayed is controlled by the application and can be modified based on user input.</span></span>

<span data-ttu-id="1c733-113">Существует два основных стиля мастера: старый стиль Wizard97 и стиль Aero, появившийся в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1c733-113">There are two main styles of wizard: the older Wizard97 style, and the Aero style introduced in Windows Vista.</span></span> <span data-ttu-id="1c733-114">Иллюстрации см. в разделе [сведения о страницах свойств](property-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="1c733-114">For illustrations, see [About Property Sheets](property-sheets.md).</span></span> <span data-ttu-id="1c733-115">(Третий стиль, используя только КОМАНДНОМ PSH \_ Wizard (мастер или \_ Мастер командном PSH \_ ). представляет собой простую последовательность страниц свойств без заголовков или водяных знаков.)</span><span class="sxs-lookup"><span data-stu-id="1c733-115">(A third style, using just the PSH\_WIZARD or PSH\_WIZARD\_LITE flag, presents a simple sequence of property sheets with no headers or watermarks.)</span></span>

> [!Note]  
> <span data-ttu-id="1c733-116">«Водяной знак» в контексте мастеров — это точечный рисунок, который отображается в левом поле некоторых страниц.</span><span class="sxs-lookup"><span data-stu-id="1c733-116">A "watermark" in the context of wizards is a bitmap that appears in the left margin of some pages.</span></span>

 

<span data-ttu-id="1c733-117">В обсуждении в большинстве случаев предполагается, что вы реализуете мастер для системы с общими элементами управления [версии 5,80](common-control-versions.md) или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1c733-117">The discussion in most of this document assumes that you are implementing a wizard for a system with [version 5.80](common-control-versions.md) or later of the common controls.</span></span> <span data-ttu-id="1c733-118">При попытке использовать стиль Wizard97 с более ранними версиями стандартных элементов управления приложение может компилироваться, но оно будет отображаться неправильно.</span><span class="sxs-lookup"><span data-stu-id="1c733-118">If you attempt to use the Wizard97 style with earlier versions of the common controls, your application may compile but it will not display properly.</span></span> <span data-ttu-id="1c733-119">Обсуждение создания мастера, совместимого с Wizard97, в более ранних системах см. в разделе мастера с поддержкой обратной совместимости далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="1c733-119">For a discussion about how to create a Wizard97-compatible wizard on earlier systems, see Backward Compatible Wizards later in this topic.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1c733-120">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="1c733-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1c733-121">Технологии</span><span class="sxs-lookup"><span data-stu-id="1c733-121">Technologies</span></span>

-   [<span data-ttu-id="1c733-122">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="1c733-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1c733-123">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1c733-123">Prerequisites</span></span>

-   <span data-ttu-id="1c733-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="1c733-124">C/C++</span></span>
-   <span data-ttu-id="1c733-125">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="1c733-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1c733-126">Инструкции</span><span class="sxs-lookup"><span data-stu-id="1c733-126">Instructions</span></span>

### <a name="wizard-implementation"></a><span data-ttu-id="1c733-127">Реализация мастера</span><span class="sxs-lookup"><span data-stu-id="1c733-127">Wizard Implementation</span></span>

<span data-ttu-id="1c733-128">Реализация мастера аналогична реализации обычной страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-128">Implementing a wizard is similar to implementing a regular property sheet.</span></span> <span data-ttu-id="1c733-129">На самом базовом уровне важно установить один из следующих флагов или сочетания флагов в структуре [**пропшисеадер**](pss-propsheetheader.md) , определяющей страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-129">At the most basic level, it is a matter of setting one of the following flags or combinations of flags in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that defines the property sheet.</span></span>



| <span data-ttu-id="1c733-130">Flag</span><span class="sxs-lookup"><span data-stu-id="1c733-130">Flag</span></span>                           | <span data-ttu-id="1c733-131">Стиль</span><span class="sxs-lookup"><span data-stu-id="1c733-131">Style</span></span>                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c733-132">\_Мастер командном PSH</span><span class="sxs-lookup"><span data-stu-id="1c733-132">PSH\_WIZARD</span></span>                    | <span data-ttu-id="1c733-133">Простой мастер без заголовков или точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="1c733-133">A simple wizard with no headers or bitmaps.</span></span>                                                                                                           |
| <span data-ttu-id="1c733-134">\_Мастер командном PSH \_ Lite</span><span class="sxs-lookup"><span data-stu-id="1c733-134">PSH\_WIZARD\_LITE</span></span>              | <span data-ttu-id="1c733-135">Аналогичен \_ мастеру командном PSH с некоторыми незначительными различиями в внешнем представлении; например, разделитель над кнопками имеет полную ширину окна.</span><span class="sxs-lookup"><span data-stu-id="1c733-135">Similar to PSH\_WIZARD, with some minor differences in appearance; for example, the divider above the buttons is set to the full width of the window.</span></span> |
| <span data-ttu-id="1c733-136">КОМАНДНОМ PSH \_ WIZARD97</span><span class="sxs-lookup"><span data-stu-id="1c733-136">PSH\_WIZARD97</span></span>                  | <span data-ttu-id="1c733-137">Мастер Wizard97 с (необязательными) заголовками, точечными рисунками заголовка и водяными знаками.</span><span class="sxs-lookup"><span data-stu-id="1c733-137">A Wizard97 wizard with (optional) headers, header bitmaps, and watermarks.</span></span>                                                                            |
| <span data-ttu-id="1c733-138">\_Мастер командном PSH \| командном PSH \_ аеровизард</span><span class="sxs-lookup"><span data-stu-id="1c733-138">PSH\_WIZARD \| PSH\_AEROWIZARD</span></span> | <span data-ttu-id="1c733-139">Мастер Aero.</span><span class="sxs-lookup"><span data-stu-id="1c733-139">An Aero Wizard.</span></span> <span data-ttu-id="1c733-140">Мастера Aero не используют водяные знаки или растровые изображения заголовков.</span><span class="sxs-lookup"><span data-stu-id="1c733-140">Aero Wizards do not use watermarks or header bitmaps.</span></span> <span data-ttu-id="1c733-141">Для них требуется модель с одним потоком апартамента (STA).</span><span class="sxs-lookup"><span data-stu-id="1c733-141">They require the single-threaded apartment (STA) model.</span></span>                         |



 

<span data-ttu-id="1c733-142">Базовая процедура реализации мастера выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c733-142">The basic procedure for implementing a wizard is as follows:</span></span>

1.  <span data-ttu-id="1c733-143">Создание шаблона диалогового окна для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-143">Create a dialog box template for each page.</span></span>
2.  <span data-ttu-id="1c733-144">Определите страницы, создав структуру [**пропшитпаже**](pss-propsheetpage.md) для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-144">Define the pages by creating a [**PROPSHEETPAGE**](pss-propsheetpage.md) structure for each page.</span></span> <span data-ttu-id="1c733-145">Эта структура определяет страницу и содержит указатели на шаблон диалогового окна и любые растровые изображения или другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1c733-145">This structure defines the page, and contains pointers to the dialog box template and any bitmaps or other resources.</span></span>
3.  <span data-ttu-id="1c733-146">Передайте структуру [**пропшитпаже**](pss-propsheetpage.md) , созданную на предыдущем шаге, в функцию [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , чтобы создать маркер хпропшитпаже страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-146">Pass the [**PROPSHEETPAGE**](pss-propsheetpage.md) structure that was created in the previous step to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function to create the page's HPROPSHEETPAGE handle.</span></span>
4.  <span data-ttu-id="1c733-147">Определите мастер, создав для него структуру [**пропшисеадер**](pss-propsheetheader.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-147">Define the wizard by creating a [**PROPSHEETHEADER**](pss-propsheetheader.md) structure for it.</span></span>
5.  <span data-ttu-id="1c733-148">Передайте структуру [**пропшисеадер**](pss-propsheetheader.md) в функцию [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) , чтобы отобразить мастер.</span><span class="sxs-lookup"><span data-stu-id="1c733-148">Pass the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to display the wizard.</span></span>
6.  <span data-ttu-id="1c733-149">Реализуйте процедуры диалоговых окон для каждой страницы, чтобы обрабатывать сообщения уведомления из элементов управления страницы и кнопки мастера, а также для обработки других сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="1c733-149">Implement dialog box procedures for each page to handle notification messages from the page's controls and the wizard's buttons and to process other Windows messaging.</span></span>

### <a name="create-the-dialog-box-templates"></a><span data-ttu-id="1c733-150">Создание шаблонов диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="1c733-150">Create the Dialog Box Templates</span></span>

<span data-ttu-id="1c733-151">Существует два основных типа страницы мастера: Наружная и внутренняя.</span><span class="sxs-lookup"><span data-stu-id="1c733-151">There are two basic types of wizard page: exterior and interior.</span></span> <span data-ttu-id="1c733-152">Внешние страницы — это введение (приветствие) и страницы завершения.</span><span class="sxs-lookup"><span data-stu-id="1c733-152">Exterior pages are the introduction (welcome) and completion pages.</span></span> <span data-ttu-id="1c733-153">Все остальные являются внутренними страницами.</span><span class="sxs-lookup"><span data-stu-id="1c733-153">All others are interior pages.</span></span>

<span data-ttu-id="1c733-154">**Шаблоны диалоговых окон «наружная страница»**</span><span class="sxs-lookup"><span data-stu-id="1c733-154">**Exterior Page Dialog Box Templates**</span></span>

<span data-ttu-id="1c733-155">Базовый макет страниц "Введение и завершение" является идентичным.</span><span class="sxs-lookup"><span data-stu-id="1c733-155">The basic layout of the introduction and completion pages is identical.</span></span> <span data-ttu-id="1c733-156">На следующем рисунке показан пример страницы введения Wizard97 с заполнителем заполнителя.</span><span class="sxs-lookup"><span data-stu-id="1c733-156">The following illustration shows a sample Wizard97 introduction page, with a placeholder watermark.</span></span>

![снимок экрана: страница мастера с изображением слева, текстом заголовка и текста, а также кнопками "назад", "Далее" и "Отмена" внизу](images/wiz97exterior.png)

<span data-ttu-id="1c733-158">Для Wizard97 наружных страниц шаблон диалогового окна представляет собой 317x193 единицы диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1c733-158">For Wizard97 exterior pages, the dialog box template is 317x193 dialog units.</span></span> <span data-ttu-id="1c733-159">Он заполняет все мастера, за исключением заголовка и полосы внизу, содержащей кнопки **назад**, **Далее** и **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="1c733-159">It fills all of the wizard, except for the caption and the band at the bottom that contains the **Back**, **Next**, and **Cancel** buttons.</span></span> <span data-ttu-id="1c733-160">Левая часть шаблона, которая зарезервирована для битовой карты "водяного знака", не должна содержать элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1c733-160">The left side of the template, which is reserved for a "watermark" bitmap, should not contain any controls.</span></span> <span data-ttu-id="1c733-161">Водяной знак указывается в структуре [**пропшисеадер**](pss-propsheetheader.md) мастера и автоматически добавляется на страницу.</span><span class="sxs-lookup"><span data-stu-id="1c733-161">The watermark is specified in the wizard's [**PROPSHEETHEADER**](pss-propsheetheader.md) structure and is added to the page automatically.</span></span> <span data-ttu-id="1c733-162">При проектировании шаблона ресурсов необходимо разрешить пространство.</span><span class="sxs-lookup"><span data-stu-id="1c733-162">You must allow space for it when designing the resource template.</span></span>

<span data-ttu-id="1c733-163">При создании растрового изображения водяного знака Помните, что размер диалогового окна может увеличиваться, если, например, пользователь выбирает большой системный шрифт.</span><span class="sxs-lookup"><span data-stu-id="1c733-163">When you create the watermark bitmap, keep in mind that the dialog box may increase in size if, for example, the user chooses a large system font.</span></span> <span data-ttu-id="1c733-164">Для разных языков также обычно применяются разные метрики шрифта.</span><span class="sxs-lookup"><span data-stu-id="1c733-164">Different languages also tend to have different font metrics.</span></span> <span data-ttu-id="1c733-165">При увеличении страницы область, зарезервированная для водяного знака, становится пропорционально увеличенной.</span><span class="sxs-lookup"><span data-stu-id="1c733-165">When the page grows, the area reserved for the watermark gets proportionately larger.</span></span> <span data-ttu-id="1c733-166">Однако нельзя изменить растровое изображение водяного знака, а также растянуть растровое изображение для заполнения большей области.</span><span class="sxs-lookup"><span data-stu-id="1c733-166">However, you cannot change the watermark bitmap, nor is the bitmap stretched to fill the larger area.</span></span> <span data-ttu-id="1c733-167">Вместо этого точечный рисунок остается в исходном размере в левой верхней части зарезервированной области.</span><span class="sxs-lookup"><span data-stu-id="1c733-167">Instead, the bitmap is left in its original size in the upper-left portion of the reserved area.</span></span> <span data-ttu-id="1c733-168">Часть более большой зарезервированной области, которая не охватывает водяного знака, автоматически заполняется цветом верхнего левого пикселя растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="1c733-168">The part of the larger reserved area that is not covered by the watermark is automatically filled with the color of the bitmap's upper-left pixel.</span></span>

<span data-ttu-id="1c733-169">Если для различных метрик шрифтов требуется использовать точечные рисунки разных размеров, то существуют два возможных решения.</span><span class="sxs-lookup"><span data-stu-id="1c733-169">If you need to have different-sized watermark bitmaps for different font metrics, two possible solutions are:</span></span>

-   <span data-ttu-id="1c733-170">Получите метрики шрифта перед созданием мастера и укажите соответствующий размер в битовом подложке.</span><span class="sxs-lookup"><span data-stu-id="1c733-170">Get the font metrics before creating the wizard, and specify an appropriately sized watermark bitmap.</span></span>
-   <span data-ttu-id="1c733-171">При создании мастера не указывайте битовую карту водяного знака.</span><span class="sxs-lookup"><span data-stu-id="1c733-171">Do not specify a watermark bitmap when you create the wizard.</span></span> <span data-ttu-id="1c733-172">Wizard97 оставляет область водяного знака пустыми.</span><span class="sxs-lookup"><span data-stu-id="1c733-172">Wizard97 will leave the watermark area blank.</span></span> <span data-ttu-id="1c733-173">Затем нарисуйте точечный рисунок соответствующего размера в области, зарезервированной для водяного знака.</span><span class="sxs-lookup"><span data-stu-id="1c733-173">Then draw an appropriately sized bitmap on the area reserved for the watermark.</span></span>

<span data-ttu-id="1c733-174">Элементы управления можно поместить в область справа от водяного знака, как в случае с обычным диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="1c733-174">You can place controls in the area to the right of the watermark as you would for a regular dialog box.</span></span> <span data-ttu-id="1c733-175">Цвет фона этой области определяется системой и не требует каких-либо действий с вашей стороны.</span><span class="sxs-lookup"><span data-stu-id="1c733-175">The background color of this area is determined by the system, and requires no action on your part.</span></span> <span data-ttu-id="1c733-176">В этой области обычно помещается два статических элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1c733-176">You typically put two static controls in this area.</span></span> <span data-ttu-id="1c733-177">Верхний элемент содержит заголовок и использует крупный полужирный шрифт (12 пт шрифт Verdana для Wizard97).</span><span class="sxs-lookup"><span data-stu-id="1c733-177">The upper one holds the title and uses a large bold font (12 point Verdana Bold for Wizard97).</span></span> <span data-ttu-id="1c733-178">Другой, для пояснительного текста, использует стандартный шрифт диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1c733-178">The other one, which is for explanatory text, uses the standard dialog box font.</span></span>

<span data-ttu-id="1c733-179">Основное различие между страницами "Введение и завершение" — это кнопки мастера и текст в статических элементах управления.</span><span class="sxs-lookup"><span data-stu-id="1c733-179">The main difference between the introduction and completion pages is the wizard buttons and the text in the static controls.</span></span> <span data-ttu-id="1c733-180">В обычных страницах обычно есть кнопка " **Далее** " и " **назад** ", для которой включена только кнопка " **Далее** ".</span><span class="sxs-lookup"><span data-stu-id="1c733-180">Introduction pages normally have a **Next** and a **Back** button, with only the **Next** button enabled.</span></span> <span data-ttu-id="1c733-181">На страницах завершения включена кнопка " **назад** ", а кнопка " **Далее** " заменяется кнопкой **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="1c733-181">Completion pages have the **Back** button enabled, and the **Next** button is replaced by a **Finish** button.</span></span>

> [!Note]  
> <span data-ttu-id="1c733-182">В мастерах Aero кнопка « **назад** » заменяется кнопкой со стрелкой в строке заголовка.</span><span class="sxs-lookup"><span data-stu-id="1c733-182">In Aero Wizards, the **Back** button is replaced by an arrow button in the caption bar.</span></span>

 

<span data-ttu-id="1c733-183">Вы можете изменить текст кнопки **Готово** , отправив мастеру сообщение [**ПСМ \_ сетфиништекст**](psm-setfinishtext.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-183">You can modify the text on the **Finish** button by sending the wizard a [**PSM\_SETFINISHTEXT**](psm-setfinishtext.md) message.</span></span> <span data-ttu-id="1c733-184">По умолчанию кнопка **Готово** не включает сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="1c733-184">By default, the **Finish** button does not include a keyboard accelerator.</span></span> <span data-ttu-id="1c733-185">Чтобы определить сочетание клавиш, включите амперсанд в текстовую строку, которую вы передали в ПСМ \_ сетфиништекст.</span><span class="sxs-lookup"><span data-stu-id="1c733-185">To define a keyboard accelerator, include an ampersand in the text string that you pass to PSM\_SETFINISHTEXT.</span></span> <span data-ttu-id="1c733-186">Например, "&Finish" определяет "F" в качестве сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="1c733-186">For instance, "&Finish" defines 'F' as the keyboard accelerator.</span></span>

<span data-ttu-id="1c733-187">**Шаблоны диалоговых окон внутренней страницы**</span><span class="sxs-lookup"><span data-stu-id="1c733-187">**Interior Page Dialog Box Templates**</span></span>

<span data-ttu-id="1c733-188">Внешний вид внутренних страниц немного отличается от внешнего вида страниц.</span><span class="sxs-lookup"><span data-stu-id="1c733-188">Interior pages have a somewhat different appearance than exterior pages.</span></span> <span data-ttu-id="1c733-189">На следующем рисунке показан пример внутренней страницы Wizard97 с битовым рисунком заполнителя заголовка.</span><span class="sxs-lookup"><span data-stu-id="1c733-189">The following illustration shows a sample Wizard97 interior page, with a placeholder header bitmap.</span></span>

![снимок экрана: страница мастера с текстом заголовка и подзаголовка, а также рисунок вверху, текст в середине и кнопки внизу](images/wiz97interior.png)

<span data-ttu-id="1c733-191">Область заголовка в верхней части страницы обрабатывается на странице свойств, поэтому она не включается в шаблон.</span><span class="sxs-lookup"><span data-stu-id="1c733-191">The header area at the top of the page is handled by the property sheet, so it is not included in the template.</span></span> <span data-ttu-id="1c733-192">Содержимое заголовка указывается в структуре [**пропшитпаже**](pss-propsheetpage.md) страницы и структуре [**пропшисеадер**](pss-propsheetheader.md) мастера.</span><span class="sxs-lookup"><span data-stu-id="1c733-192">The contents of the header are specified in the page's [**PROPSHEETPAGE**](pss-propsheetpage.md) structure and the wizard's [**PROPSHEETHEADER**](pss-propsheetheader.md) structure.</span></span> <span data-ttu-id="1c733-193">Так как внутренняя страница должна соответствовать заголовку и кнопкам, шаблон диалогового окна Wizard97 — это 317x143 единицы диалогового окна, немного меньше, чем шаблон для наружных страниц.</span><span class="sxs-lookup"><span data-stu-id="1c733-193">Because the interior page needs to fit between the header and the buttons, the Wizard97 dialog box template is 317x143 dialog units, somewhat smaller than the template for exterior pages.</span></span>

<span data-ttu-id="1c733-194">На следующем рисунке показан мастер Aero, созданный из того же шаблона.</span><span class="sxs-lookup"><span data-stu-id="1c733-194">The following illustration shows an Aero Wizard that was created from the same template.</span></span>

![снимок экрана, отличающийся от предыдущего, с заполнением области заголовка сверху, только кнопками "Далее" и "Отмена" внизу](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a><span data-ttu-id="1c733-196">Определение страниц мастера</span><span class="sxs-lookup"><span data-stu-id="1c733-196">Define the Wizard Pages</span></span>

<span data-ttu-id="1c733-197">После создания шаблонов диалоговых окон и связанных ресурсов, таких как точечные рисунки и таблицы строк, можно создать страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-197">After you have created the dialog box templates and related resources such as bitmaps and string tables, you can create the property sheet pages.</span></span> <span data-ttu-id="1c733-198">Процедура аналогична процедуре для стандартных вкладок свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-198">The procedure is similar to that for standard property sheets.</span></span> <span data-ttu-id="1c733-199">Сначала заполните соответствующие элементы структуры [**пропшитпаже**](pss-propsheetpage.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-199">First, fill in the appropriate members of a [**PROPSHEETPAGE**](pss-propsheetpage.md) structure.</span></span> <span data-ttu-id="1c733-200">(Некоторые члены относятся только к мастерам.) Затем вызовите функцию [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , чтобы создать обработчик хпропшитпаже страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-200">(Some members are specific to wizards.) Then call the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function to create the page's HPROPSHEETPAGE handle.</span></span>

<span data-ttu-id="1c733-201">Следующие флаги, связанные с мастером, можно задать в элементе **dwFlags** структуры [**пропшитпаже**](pss-propsheetpage.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-201">The following wizard-related flags can be set in the **dwFlags** member of the [**PROPSHEETPAGE**](pss-propsheetpage.md) structure.</span></span>



| <span data-ttu-id="1c733-202">Flag</span><span class="sxs-lookup"><span data-stu-id="1c733-202">Flag</span></span>                   | <span data-ttu-id="1c733-203">Описание</span><span class="sxs-lookup"><span data-stu-id="1c733-203">Description</span></span>                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c733-204">PSP \_ хидехеадер</span><span class="sxs-lookup"><span data-stu-id="1c733-204">PSP\_HIDEHEADER</span></span>        | <span data-ttu-id="1c733-205">Установите этот флаг для наружных страниц в Wizard97.</span><span class="sxs-lookup"><span data-stu-id="1c733-205">Set this flag for exterior pages in Wizard97.</span></span> <span data-ttu-id="1c733-206">Заголовок не отображается, и можно отобразить водяной знак.</span><span class="sxs-lookup"><span data-stu-id="1c733-206">The header is not shown, and a watermark can be shown.</span></span>                                |
| <span data-ttu-id="1c733-207">PSP \_ усехеадертитле</span><span class="sxs-lookup"><span data-stu-id="1c733-207">PSP\_USEHEADERTITLE</span></span>    | <span data-ttu-id="1c733-208">Установите этот флаг для внутренних страниц, чтобы разместить заголовок в области заголовка в Wizard97 или в верхней части клиентской области в мастере Aero.</span><span class="sxs-lookup"><span data-stu-id="1c733-208">Set this flag for interior pages to put a title in the header area in Wizard97, or at the top of the client area in an Aero Wizard.</span></span> |
| <span data-ttu-id="1c733-209">PSP \_ усехеадерсубтитле</span><span class="sxs-lookup"><span data-stu-id="1c733-209">PSP\_USEHEADERSUBTITLE</span></span> | <span data-ttu-id="1c733-210">Установите этот флаг для внутренних страниц, чтобы разместить подзаголовок в области заголовка в Wizard97.</span><span class="sxs-lookup"><span data-stu-id="1c733-210">Set this flag for interior pages to put a subtitle in the header area in Wizard97.</span></span>                                                  |



 

<span data-ttu-id="1c733-211">Если вы установили PSP \_ усехеадертитле или PSP \_ усехеадерсубтитле, назначьте заголовок и подзаголовок членам **псзеадертитле** и **псзеадерсубтитле** соответственно.</span><span class="sxs-lookup"><span data-stu-id="1c733-211">If you have set PSP\_USEHEADERTITLE or PSP\_USEHEADERSUBTITLE, assign the title and subtitle text to the **pszHeaderTitle** and **pszHeaderSubtitle** members, respectively.</span></span> <span data-ttu-id="1c733-212">При присваивании текстовых строк членам структур [**пропшитпаже**](pss-propsheetpage.md) и [**пропшисеадер**](pss-propsheetheader.md) можно либо назначить указатель строки, либо использовать макрос **макеинтресаурце** для назначения значения из строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="1c733-212">When you assign text strings to members of the [**PROPSHEETPAGE**](pss-propsheetpage.md) and [**PROPSHEETHEADER**](pss-propsheetheader.md) structures, you can either assign a string pointer or use the **MAKEINTRESOURCE** macro to assign a value from a string resource.</span></span> <span data-ttu-id="1c733-213">Строковый ресурс загружается из модуля, указанного в элементе **HINSTANCE** структуры **пропшисеадер** мастера.</span><span class="sxs-lookup"><span data-stu-id="1c733-213">The string resource is loaded from the module specified in the **hInstance** member of the wizard's **PROPSHEETHEADER** structure.</span></span>

<span data-ttu-id="1c733-214">При вызове [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) для создания страницы присвойте результат элементу массива дескрипторов хпропшитпаже.</span><span class="sxs-lookup"><span data-stu-id="1c733-214">When you call [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) to create a page, assign the result to an element of an array of HPROPSHEETPAGE handles.</span></span> <span data-ttu-id="1c733-215">Этот массив используется при создании страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-215">This array is used when creating the property sheet.</span></span> <span data-ttu-id="1c733-216">Индекс массива для маркера страницы определяет порядок, в котором он отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c733-216">The array index of a page's handle determines the default order in which it is displayed.</span></span> <span data-ttu-id="1c733-217">После создания обработчика ХПРОПШИТПАЖЕ страницы можно повторно использовать ту же структуру [**пропшитпаже**](pss-propsheetpage.md) , чтобы создать следующую страницу путем назначения новых значений соответствующим элементам.</span><span class="sxs-lookup"><span data-stu-id="1c733-217">After you have created a page's HPROPSHEETPAGE handle, you can reuse the same [**PROPSHEETPAGE**](pss-propsheetpage.md) structure to create the next page by assigning new values to the relevant members.</span></span>

<span data-ttu-id="1c733-218">Альтернативным способом создания страниц является использование отдельных структур [**пропшитпаже**](pss-propsheetpage.md) для каждой страницы и создание массива структур.</span><span class="sxs-lookup"><span data-stu-id="1c733-218">An alternative way to create pages is to use separate [**PROPSHEETPAGE**](pss-propsheetpage.md) structures for each page, and create an array of structures.</span></span> <span data-ttu-id="1c733-219">Этот массив используется вместо массива дескрипторов ХПРОПШИТПАЖЕ при создании страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-219">This array is used instead of an array of HPROPSHEETPAGE handles when creating the property sheet.</span></span> <span data-ttu-id="1c733-220">Использование отдельных структур **пропшитпаже** исключает необходимость вызова [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , но использует больше памяти.</span><span class="sxs-lookup"><span data-stu-id="1c733-220">Using separate **PROPSHEETPAGE** structures eliminates the need to call [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) but uses more memory.</span></span> <span data-ttu-id="1c733-221">В противном случае существенная разница между двумя подходами отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1c733-221">Otherwise, there is no significant difference between the two approaches.</span></span>

<span data-ttu-id="1c733-222">В следующем примере определяется внутренняя страница Wizard97 путем присвоения значений структуре [**пропшитпаже**](pss-propsheetpage.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-222">The following example defines an interior Wizard97 page by assigning values to a [**PROPSHEETPAGE**](pss-propsheetpage.md) structure.</span></span> <span data-ttu-id="1c733-223">В этом примере заголовок страницы, подзаголовок и шаблон диалогового окна определяются по идентификаторам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c733-223">In this example, the page's title, subtitle, and dialog box template are all identified by their resource IDs.</span></span> <span data-ttu-id="1c733-224">Затем вызывается функция [**креатепропертишитпаже**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) для создания маркера хпропшитпаже страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-224">The [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function is then called to create the page's HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="1c733-225">Так как это будет вторая страница, то дескриптор присваивается массиву дескрипторов *ахпсп* с индексом 1.</span><span class="sxs-lookup"><span data-stu-id="1c733-225">Because it will be the second page to appear, the handle is assigned to the array of handles, *ahpsp*, with an index of 1.</span></span>


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a><span data-ttu-id="1c733-226">Настраиваемые данные страницы</span><span class="sxs-lookup"><span data-stu-id="1c733-226">Custom Page Data</span></span>

<span data-ttu-id="1c733-227">При создании страницы к ней можно присвоить пользовательские данные с помощью члена **lParam** структуры [**пропшитпаже**](pss-propsheetpage.md) , обычно путем присвоения ей указателя на определяемую пользователем структуру.</span><span class="sxs-lookup"><span data-stu-id="1c733-227">When you create a page, you can assign custom data to it by using the **lParam** member of the [**PROPSHEETPAGE**](pss-propsheetpage.md) structure, typically by assigning it a pointer to a user-defined structure.</span></span>

<span data-ttu-id="1c733-228">При первом выборе страницы процедура диалогового окна получает сообщение [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="1c733-228">When the page is first selected, its dialog box procedure receives a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="1c733-229">Значение *lParam* сообщения указывает на копию структуры [**пропшитпаже**](pss-propsheetpage.md) страницы, из которой можно получить пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="1c733-229">The message's *lParam* value points to a copy of of the page's [**PROPSHEETPAGE**](pss-propsheetpage.md) structure, from which you can retrieve the custom data.</span></span> <span data-ttu-id="1c733-230">Затем эти данные можно сохранить для использования в последующих сообщениях с помощью [**сетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) с ГВЛ \_ USERDATA в качестве параметра индекса.</span><span class="sxs-lookup"><span data-stu-id="1c733-230">You can then store this data for use in subsequent messages by using [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) with GWL\_USERDATA as the index parameter.</span></span> <span data-ttu-id="1c733-231">Несколько страниц могут иметь указатель на одни и те же данные, и любые изменения данных, внесенные одной страницей, доступны другим страницам в процедурах диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1c733-231">Multiple pages can have a pointer to the same data, and any change to the data made by one page is available to the other pages in their dialog procedures.</span></span>

### <a name="define-the-wizard-property-sheet"></a><span data-ttu-id="1c733-232">Определение страницы свойств мастера</span><span class="sxs-lookup"><span data-stu-id="1c733-232">Define the Wizard Property Sheet</span></span>

<span data-ttu-id="1c733-233">Как и в случае с обычными страницами свойств, можно определить страницу свойств мастера, заполнив элементы структуры [**пропшисеадер**](pss-propsheetheader.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-233">As with ordinary property sheets, you define the wizard's property sheet by filling in members of a [**PROPSHEETHEADER**](pss-propsheetheader.md) structure.</span></span> <span data-ttu-id="1c733-234">Эта структура позволяет указать страницы, составляющие мастер, и порядок, в котором они будут отображаться, а также несколько связанных параметров.</span><span class="sxs-lookup"><span data-stu-id="1c733-234">This structure allows you to specify the pages that make up the wizard and the default order in which they are displayed, along with several related parameters.</span></span> <span data-ttu-id="1c733-235">Затем запустите мастер, вызвав функцию [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .</span><span class="sxs-lookup"><span data-stu-id="1c733-235">You then launch the wizard by calling the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

<span data-ttu-id="1c733-236">В стиле Wizard97 элемент **псзкаптион** структуры [**пропшисеадер**](pss-propsheetheader.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1c733-236">In the Wizard97 style, the **pszCaption** member of the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure is ignored.</span></span> <span data-ttu-id="1c733-237">Вместо этого мастер отображает заголовок, указанный в шаблоне диалогового окна текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-237">Instead, the wizard displays the caption that is specified in the current page's dialog box template.</span></span> <span data-ttu-id="1c733-238">Если в шаблоне отсутствует заголовок, отображается заголовок из предыдущей страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-238">If the template lacks a caption, the caption from the previous page is displayed.</span></span> <span data-ttu-id="1c733-239">Таким же, чтобы отобразить один и тот же заголовок на всех страницах, укажите заголовок в шаблоне для вводной страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-239">Thus, to display the same caption on all pages, specify the caption in the template for the introductory page.</span></span>

<span data-ttu-id="1c733-240">В стиле мастера Aero заголовок диалогового окна берется из **псзкаптион**.</span><span class="sxs-lookup"><span data-stu-id="1c733-240">In the Aero Wizard style, the dialog box caption is taken from **pszCaption**.</span></span>

<span data-ttu-id="1c733-241">Если вы создали массив дескрипторов ХПРОПШИТПАЖЕ для страниц, назначьте массив элементу **фпаже** .</span><span class="sxs-lookup"><span data-stu-id="1c733-241">If you have created an array of HPROPSHEETPAGE handles for your pages, assign the array to the **phpage** member.</span></span> <span data-ttu-id="1c733-242">Если вместо этого был создан массив структур [**пропшитпаже**](pss-propsheetpage.md) , назначьте массив элементу **ППСП** и установите \_ флаг командном PSH пропшитпаже в элементе **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="1c733-242">If you have instead created an array of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures, assign the array to the **ppsp** member and set the PSH\_PROPSHEETPAGE flag in the **dwFlags** member.</span></span>

<span data-ttu-id="1c733-243">В следующем примере значения присваиваются *командном PSH*, структуре [**пропшисеадер**](pss-propsheetheader.md) и вызывается функция [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) для запуска мастера.</span><span class="sxs-lookup"><span data-stu-id="1c733-243">The following example assigns values to *psh*, a [**PROPSHEETHEADER**](pss-propsheetheader.md) structure, and calls the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to launch the wizard.</span></span> <span data-ttu-id="1c733-244">В мастере Wizard97 имеется как водяной знак, так и рисунок заголовка, определяемые их идентификаторами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c733-244">The Wizard97-style wizard has both watermark and header graphics, specified by their resource IDs.</span></span> <span data-ttu-id="1c733-245">Массив *ахпсп* содержит все дескрипторы хпропшитпаже и определяет порядок по умолчанию, в котором они отображаются.</span><span class="sxs-lookup"><span data-stu-id="1c733-245">The *ahpsp* array contains all the HPROPSHEETPAGE handles and defines the default order in which they are displayed.</span></span>


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a><span data-ttu-id="1c733-246">Процедура диалогового окна</span><span class="sxs-lookup"><span data-stu-id="1c733-246">The Dialog Box Procedure</span></span>

<span data-ttu-id="1c733-247">Каждой странице мастера требуется процедура диалогового окна для обработки сообщений Windows, в частности уведомлений от его элементов управления и мастера.</span><span class="sxs-lookup"><span data-stu-id="1c733-247">Each page of the wizard needs a dialog box procedure to process Windows messages, particularly notifications from its controls and the wizard.</span></span> <span data-ttu-id="1c733-248">Три сообщения, которые должны быть способны обрабатывать почти все мастера: [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog), [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy)и [**WM \_ Notify**](wm-notify.md).</span><span class="sxs-lookup"><span data-stu-id="1c733-248">The three messages that almost all wizards must be able to handle are [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog), [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), and [**WM\_NOTIFY**](wm-notify.md).</span></span>

<span data-ttu-id="1c733-249">Сообщение [**WM \_ Notify**](wm-notify.md) получается перед отображением страницы и нажатием кнопки мастера.</span><span class="sxs-lookup"><span data-stu-id="1c733-249">The [**WM\_NOTIFY**](wm-notify.md) message is received before the page is displayed and when any of the wizard's buttons are clicked.</span></span> <span data-ttu-id="1c733-250">Параметр *lParam* сообщения является указателем на структуру заголовков [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="1c733-250">The *lParam* parameter of the message is a pointer to a [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) header structure.</span></span> <span data-ttu-id="1c733-251">Идентификатор уведомления содержится в элементе **кода** структуры.</span><span class="sxs-lookup"><span data-stu-id="1c733-251">The notification's ID is contained in the structure's **code** member.</span></span> <span data-ttu-id="1c733-252">Ниже приведены четыре уведомления, которые должны быть обработаны большинством мастеров.</span><span class="sxs-lookup"><span data-stu-id="1c733-252">The four notifications that most wizards need to handle are the following.</span></span>



| <span data-ttu-id="1c733-253">Код</span><span class="sxs-lookup"><span data-stu-id="1c733-253">Code</span></span>                                | <span data-ttu-id="1c733-254">Описание</span><span class="sxs-lookup"><span data-stu-id="1c733-254">Description</span></span>                                 |
|-------------------------------------|---------------------------------------------|
| [<span data-ttu-id="1c733-255">PSN \_ сетактиве</span><span class="sxs-lookup"><span data-stu-id="1c733-255">PSN\_SETACTIVE</span></span>](psn-setactive.md) | <span data-ttu-id="1c733-256">Отправляется перед отображением страницы.</span><span class="sxs-lookup"><span data-stu-id="1c733-256">Sent before the page is displayed.</span></span>          |
| [<span data-ttu-id="1c733-257">PSN \_ визбакк</span><span class="sxs-lookup"><span data-stu-id="1c733-257">PSN\_WIZBACK</span></span>](psn-wizback.md)     | <span data-ttu-id="1c733-258">Посылается при нажатии кнопки " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="1c733-258">Sent when the **Back** button is clicked.</span></span>   |
| [<span data-ttu-id="1c733-259">PSN \_ визнекст</span><span class="sxs-lookup"><span data-stu-id="1c733-259">PSN\_WIZNEXT</span></span>](psn-wiznext.md)     | <span data-ttu-id="1c733-260">Посылается при нажатии кнопки " **Далее** ".</span><span class="sxs-lookup"><span data-stu-id="1c733-260">Sent when the **Next** button is clicked.</span></span>   |
| [<span data-ttu-id="1c733-261">PSN \_ визфиниш</span><span class="sxs-lookup"><span data-stu-id="1c733-261">PSN\_WIZFINISH</span></span>](psn-wizfinish.md) | <span data-ttu-id="1c733-262">Отправляется при нажатии кнопки **"Готово"** .</span><span class="sxs-lookup"><span data-stu-id="1c733-262">Sent when the **Finish** button is clicked.</span></span> |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a><span data-ttu-id="1c733-263">Handles WM \_ инитдиалог и WM \_ destroy</span><span class="sxs-lookup"><span data-stu-id="1c733-263">Handle WM\_INITDIALOG and WM\_DESTROY</span></span>

<span data-ttu-id="1c733-264">Когда страница собирается отображаться в первый раз, ее процедура диалогового окна получает сообщение [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="1c733-264">When a page is about to be displayed for the first time, its dialog box procedure receives a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="1c733-265">Обработка этого сообщения позволяет мастеру выполнить необходимые задачи инициализации, такие как хранение пользовательских данных или установка шрифтов.</span><span class="sxs-lookup"><span data-stu-id="1c733-265">Handling this message allows the wizard to do any needed initialization tasks, such as storing custom data or setting fonts.</span></span>

<span data-ttu-id="1c733-266">При удалении страницы свойств появляется сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="1c733-266">When the property sheet is destroyed, you receive a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="1c733-267">Мастер автоматически уничтожается системой, но обработка этого сообщения позволяет выполнить все необходимые действия по очистке.</span><span class="sxs-lookup"><span data-stu-id="1c733-267">The wizard is automatically destroyed by the system, but handling this message allows you to do any needed cleanup.</span></span>

### <a name="handle-psn_setactive"></a><span data-ttu-id="1c733-268">Обработайте PSN \_ сетактиве</span><span class="sxs-lookup"><span data-stu-id="1c733-268">Handle PSN\_SETACTIVE</span></span>

<span data-ttu-id="1c733-269">Код уведомления [PSN \_ сетактиве](psn-setactive.md) отправляется каждый раз, когда страница собирается сделать видимой.</span><span class="sxs-lookup"><span data-stu-id="1c733-269">The [PSN\_SETACTIVE](psn-setactive.md) notification code is sent each time a page is about to be made visible.</span></span> <span data-ttu-id="1c733-270">При первом посещении страницы PSN \_ сетактиве следует за сообщением [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="1c733-270">The first time a page is visited, PSN\_SETACTIVE follows the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="1c733-271">Если страница впоследствии снова посещается, она получает только \_ уведомление PSN сетактиве.</span><span class="sxs-lookup"><span data-stu-id="1c733-271">If the page is subsequently revisited, it receives only a PSN\_SETACTIVE notification.</span></span> <span data-ttu-id="1c733-272">Это уведомление обычно обрабатывается для инициализации данных на странице и включения соответствующих кнопок.</span><span class="sxs-lookup"><span data-stu-id="1c733-272">This notification is usually handled to initialize data for the page and enable the appropriate buttons.</span></span>

<span data-ttu-id="1c733-273">По умолчанию в мастере отображаются кнопки **назад**, **Далее** и **Отмена** , для которых включены все кнопки.</span><span class="sxs-lookup"><span data-stu-id="1c733-273">By default, the wizard displays **Back**, **Next**, and **Cancel** buttons, with all buttons enabled.</span></span> <span data-ttu-id="1c733-274">Чтобы отключить кнопку или отобразить **Окончание** , а не **Далее**, необходимо отправить сообщение [**ПСМ \_ сетвизбуттонс**](psm-setwizbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-274">To disable a button or display **Finish** instead of **Next**, you must send a [**PSM\_SETWIZBUTTONS**](psm-setwizbuttons.md) message.</span></span> <span data-ttu-id="1c733-275">После отправки сообщения состояние кнопок сохраняется до тех пор, пока оно не будет изменено другим сообщением **ПСМ \_ сетвизбуттонс** , даже если выбрана новая страница.</span><span class="sxs-lookup"><span data-stu-id="1c733-275">After this message has been sent, the state of the buttons is preserved until it is modified by another **PSM\_SETWIZBUTTONS** message, even if a new page is selected.</span></span> <span data-ttu-id="1c733-276">Как правило, все обработчики [ \_ сетактиве PSN](psn-setactive.md) отправляют это сообщение, чтобы убедиться, что каждая страница имеет правильное состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="1c733-276">Typically, all [PSN\_SETACTIVE](psn-setactive.md) handlers send this message to ensure that each page has the correct button state.</span></span>

<span data-ttu-id="1c733-277">Состояние кнопки можно изменить с помощью этого сообщения в любое время.</span><span class="sxs-lookup"><span data-stu-id="1c733-277">You can change the button state with this message at any time.</span></span> <span data-ttu-id="1c733-278">Например, может потребоваться изначально отключить кнопку " **Далее** ".</span><span class="sxs-lookup"><span data-stu-id="1c733-278">For example, you may want the **Next** button to be initially disabled.</span></span> <span data-ttu-id="1c733-279">После того как пользователь указал все необходимые сведения, можно отправить другое сообщение [**ПСМ \_ сетвизбуттонс**](psm-setwizbuttons.md) , чтобы включить кнопку **Далее** и позволить пользователю перейти на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="1c733-279">After a user has entered all the necessary information, you can send another [**PSM\_SETWIZBUTTONS**](psm-setwizbuttons.md) message to enable the **Next** button and let the user proceed to the next page.</span></span>

<span data-ttu-id="1c733-280">В следующем фрагменте кода используется макрос [**пропшит \_ сетвизбуттонс**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) для включения кнопок " **назад** " и " **Далее** " на внутренней странице перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="1c733-280">The following code fragment uses the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to enable the **Back** and **Next** buttons on an interior page before it is displayed.</span></span>


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a><span data-ttu-id="1c733-281">Работа с PSN \_ визнекст, пснвизбакк и PSN \_ визфиниш</span><span class="sxs-lookup"><span data-stu-id="1c733-281">Handle PSN\_WIZNEXT, PSNWIZBACK, and PSN\_WIZFINISH</span></span>

<span data-ttu-id="1c733-282">При нажатии кнопки " **Далее** " или " **назад** " вы получаете код уведомления [PSN \_ визнекст](psn-wiznext.md) или [PSN \_ визбакк](psn-wizback.md) .</span><span class="sxs-lookup"><span data-stu-id="1c733-282">When a **Next** or **Back** button is clicked, you receive a [PSN\_WIZNEXT](psn-wiznext.md) or [PSN\_WIZBACK](psn-wizback.md) notification code.</span></span> <span data-ttu-id="1c733-283">По умолчанию мастер автоматически переходит на следующую или предыдущую страницу в порядке, определенном при создании страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1c733-283">By default, the wizard automatically goes to either the next or previous page in the order that is defined when the property sheet is created.</span></span> <span data-ttu-id="1c733-284">Распространенной причиной для решения этих уведомлений является запрет пользователю переключать страницы или переопределять порядок страниц по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c733-284">A common reason to handle these notifications is to prevent the user from switching pages, or to override the default page order.</span></span>

<span data-ttu-id="1c733-285">Чтобы запретить пользователю переключать страницы, обработайте уведомление кнопки, вызовите функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с параметром DWL \_ мсгресулт со значением – 1 и возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1c733-285">To prevent the user from switching pages, handle the button notification, call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value set to –1, and return **TRUE**.</span></span> <span data-ttu-id="1c733-286">Пример:</span><span class="sxs-lookup"><span data-stu-id="1c733-286">For example:</span></span>


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



<span data-ttu-id="1c733-287">Чтобы переопределить стандартный порядок и переходить на определенную страницу, вызовите [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с параметром DWL \_ мсгресулт, установленным в поле Идентификатор ресурса диалогового окна страницы, и возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1c733-287">To override the standard order and go to a particular page, call [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) with the DWL\_MSGRESULT value set to the page's dialog box resource ID, and return **TRUE**.</span></span> <span data-ttu-id="1c733-288">Пример:</span><span class="sxs-lookup"><span data-stu-id="1c733-288">For example:</span></span>


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



<span data-ttu-id="1c733-289">При нажатии кнопки **"Готово"** или **"Отмена** " вы получаете код уведомления [PSN \_ визфиниш](psn-wizfinish.md) или [PSN \_ Reset](psn-reset.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="1c733-289">When the **Finish** or **Cancel** button is clicked, you receive a [PSN\_WIZFINISH](psn-wizfinish.md) or [PSN\_RESET](psn-reset.md) notification code, respectively.</span></span> <span data-ttu-id="1c733-290">При нажатии любой из этих кнопок мастер автоматически уничтожается системой.</span><span class="sxs-lookup"><span data-stu-id="1c733-290">When either of these buttons is clicked, the wizard is automatically destroyed by the system.</span></span> <span data-ttu-id="1c733-291">Однако эти уведомления можно обрабатывайте, если необходимо выполнить задачи очистки до уничтожения мастера.</span><span class="sxs-lookup"><span data-stu-id="1c733-291">However, you can handle these notifications if you need to perform cleanup tasks before the wizard is destroyed.</span></span> <span data-ttu-id="1c733-292">Чтобы предотвратить уничтожение мастера при получении \_ уведомления PSN визфиниш, вызовите [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с параметром DWL мсгресулт, \_ установленным в значение **true**, и возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1c733-292">To prevent the wizard from being destroyed when you receive a PSN\_WIZFINISH notification, call [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) with the DWL\_MSGRESULT value set to **TRUE**, and return **TRUE**.</span></span> <span data-ttu-id="1c733-293">Пример:</span><span class="sxs-lookup"><span data-stu-id="1c733-293">For example:</span></span>


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a><span data-ttu-id="1c733-294">Мастера с обратной совместимостью</span><span class="sxs-lookup"><span data-stu-id="1c733-294">Backward Compatible Wizards</span></span>

<span data-ttu-id="1c733-295">В предыдущем разделе предполагается, что вы реализуете мастер для системы с общими элементами управления [версии 5](common-control-versions.md) или более поздней.</span><span class="sxs-lookup"><span data-stu-id="1c733-295">The preceding section assumes that you are implementing a wizard for a system with [version 5](common-control-versions.md) or later of the common controls.</span></span>

<span data-ttu-id="1c733-296">При написании мастера для систем с более ранними версиями стандартных элементов управления многие функции, описанные в предыдущем разделе, будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="1c733-296">If you are writing a wizard for systems with earlier versions of the common controls, many of the features discussed in the preceding section will not be available.</span></span> <span data-ttu-id="1c733-297">Ряд элементов структур [**пропшисеадер**](pss-propsheetheader.md) и [**пропшитпаже**](pss-propsheetpage.md) , используемых стилем Wizard97, поддерживается только для стандартных элементов управления версии 5 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="1c733-297">A number of the members of the [**PROPSHEETHEADER**](pss-propsheetheader.md) and [**PROPSHEETPAGE**](pss-propsheetpage.md) structures that are used by the Wizard97 style are supported only by common controls version 5 and later.</span></span> <span data-ttu-id="1c733-298">Однако по-прежнему можно реализовать мастер *обратной совместимости* с внешним видом, похожим на стиль стиля Wizard97.</span><span class="sxs-lookup"><span data-stu-id="1c733-298">However, it is still possible to implement a *backward compatible* wizard with an appearance similar to that of the Wizard97 style.</span></span> <span data-ttu-id="1c733-299">Для этого необходимо явно реализовать следующее:</span><span class="sxs-lookup"><span data-stu-id="1c733-299">To do so, you must explicitly implement the following:</span></span>

-   <span data-ttu-id="1c733-300">Добавьте рисунок водяного знака в шаблон диалогового окна для страниц "Введение и завершение".</span><span class="sxs-lookup"><span data-stu-id="1c733-300">Add the watermark graphic to the dialog box template for your introduction and completion pages.</span></span>
-   <span data-ttu-id="1c733-301">Сделайте все шаблоны одинаковым размером.</span><span class="sxs-lookup"><span data-stu-id="1c733-301">Make all your templates the same size.</span></span> <span data-ttu-id="1c733-302">Для внутренних страниц не существует отдельной определенной системой области заголовка.</span><span class="sxs-lookup"><span data-stu-id="1c733-302">There is no separate system-defined header area for interior pages.</span></span>
-   <span data-ttu-id="1c733-303">Явно создайте область заголовка внутренней страницы в шаблонах.</span><span class="sxs-lookup"><span data-stu-id="1c733-303">Create the interior page's header area explicitly on your templates.</span></span>
-   <span data-ttu-id="1c733-304">Не используйте изображение заголовка, так как оно может конфликтовать с заголовком или подзаголовок, если размер мастера изменяется.</span><span class="sxs-lookup"><span data-stu-id="1c733-304">Do not use a header graphic because it may conflict with the title or subtitle if the wizard changes size.</span></span>

<span data-ttu-id="1c733-305">Дополнительные сведения о мастерах с поддержкой обратной совместимости см. в статье [Мастер обратной совместимости 97](/previous-versions//ms737910(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c733-305">For further discussion of backward-compatible wizards, see [Backward Compatible Wizard 97](/previous-versions//ms737910(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c733-306">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c733-306">Remarks</span></span>

<span data-ttu-id="1c733-307">Полное описание проблем проектирования для Wizard97 см. в разделе [Спецификация Wizard97](/previous-versions//ms738248(v=vs.85))в других Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1c733-307">For a complete discussion of design issues for Wizard97, see the [Wizard97 Specification](/previous-versions//ms738248(v=vs.85)), elsewhere in the Windows SDK.</span></span> <span data-ttu-id="1c733-308">В этом документе приводятся рекомендации по таким принципам, как измерения для диалоговых окон, растровые измерения и цвета, а также размещение элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1c733-308">This document has guidelines for such things as the dimensions for the dialog boxes, bitmap dimensions and colors, and the placement of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c733-309">См. также</span><span class="sxs-lookup"><span data-stu-id="1c733-309">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c733-310">Использование страниц свойств</span><span class="sxs-lookup"><span data-stu-id="1c733-310">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="1c733-311">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1c733-311">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 