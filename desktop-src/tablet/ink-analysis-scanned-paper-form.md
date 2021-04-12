---
description: В этом образце показано, как использовать анализ рукописного ввода для создания приложения заполнения форм, в котором форма основана на отсканированной бумажной форме.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Бумажная форма анализа рукописного текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262902"
---
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="b38e0-103">Бумажная форма анализа рукописного текста</span><span class="sxs-lookup"><span data-stu-id="b38e0-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="b38e0-104">В этом образце показано, как использовать анализ рукописного ввода для создания приложения заполнения форм, в котором форма основана на отсканированной бумажной форме.</span><span class="sxs-lookup"><span data-stu-id="b38e0-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="b38e0-105">Демонстрируемые возможности</span><span class="sxs-lookup"><span data-stu-id="b38e0-105">Features Demonstrated</span></span>

<span data-ttu-id="b38e0-106">В этом примере приложения демонстрируются следующие возможности API анализа рукописного ввода и Windows Forms элементов управления рукописного ввода:</span><span class="sxs-lookup"><span data-stu-id="b38e0-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="b38e0-107">Загрузка печатной формы.</span><span class="sxs-lookup"><span data-stu-id="b38e0-107">Loading a scanned paper form.</span></span> <span data-ttu-id="b38e0-108">В этом примере форма импортируется из изображения в формате PNG.</span><span class="sxs-lookup"><span data-stu-id="b38e0-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="b38e0-109">Сбор и отрисовка рукописного ввода поверх сканируемой формы.</span><span class="sxs-lookup"><span data-stu-id="b38e0-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="b38e0-110">Использование объекта [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) для анализа рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="b38e0-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="b38e0-111">Создание объектов [аналисишинтноде](/previous-versions/ms573018(v=vs.100)) для улучшения результатов рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b38e0-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="b38e0-112">Заполнение текстовых полей в подсказках анализа.</span><span class="sxs-lookup"><span data-stu-id="b38e0-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="b38e0-113">Создание базовой работы по исправлению текста.</span><span class="sxs-lookup"><span data-stu-id="b38e0-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="b38e0-114">Ссылки проекта</span><span class="sxs-lookup"><span data-stu-id="b38e0-114">Project References</span></span>

<span data-ttu-id="b38e0-115">Пример доступен в виде приложения Windows Forms или Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="b38e0-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="b38e0-116">Ссылки на Windows Forms версии:</span><span class="sxs-lookup"><span data-stu-id="b38e0-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="b38e0-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="b38e0-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="b38e0-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="b38e0-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="b38e0-119">Версия Windows Presentation Foundation ссылается на IAWinFX.dll в дополнение к основным Windows Presentation Foundation библиотекам DLL.</span><span class="sxs-lookup"><span data-stu-id="b38e0-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="b38e0-120">Для Windows Presentation Foundation версии этого образца (найден в каталоге XAML) требуется, чтобы в системе были установлены расширения Windows Presentation Foundation для Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="b38e0-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="b38e0-121">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="b38e0-121">User Interface</span></span>

<span data-ttu-id="b38e0-122">Пользовательский интерфейс для этого приложения состоит из элемента [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) с двумя связанными объектами [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) : рукописная форма и преобразованная Текстовая форма.</span><span class="sxs-lookup"><span data-stu-id="b38e0-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="b38e0-123">Вкладка форма рукописного ввода содержит</span><span class="sxs-lookup"><span data-stu-id="b38e0-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="b38e0-124">Панель, содержащая изображение печатной формы, используемой для получения телефонных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b38e0-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="b38e0-125">Флажок, имеющий приложение, отображает границы подсказок анализа при выборе.</span><span class="sxs-lookup"><span data-stu-id="b38e0-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="b38e0-126">Пара кнопок, очищает и анализирует, которые очищают рукописный ввод из формы и инициализируют анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b38e0-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="b38e0-127">Преобразованная Текстовая форма содержит то же изображение, а — страницу, на которой приложение отображает распознанный текст.</span><span class="sxs-lookup"><span data-stu-id="b38e0-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="b38e0-128">При нажатии кнопки анализ приложение выполняет анализ рукописного ввода в синхронном режиме, а результаты распознавания отображаются на вкладке преобразованная Текстовая форма.</span><span class="sxs-lookup"><span data-stu-id="b38e0-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="b38e0-129">Функциональность</span><span class="sxs-lookup"><span data-stu-id="b38e0-129">Functionality</span></span>

<span data-ttu-id="b38e0-130">Это приложение использует [InkOverlay](/previous-versions/ms552322(v=vs.100)) для включения записи.</span><span class="sxs-lookup"><span data-stu-id="b38e0-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="b38e0-131">Объект InkOverlay хорошо подходит для создания заметок и создания базовых кривых.</span><span class="sxs-lookup"><span data-stu-id="b38e0-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="b38e0-132">Основным предполагаемым использованием этого объекта является отображение рукописных данных в виде рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="b38e0-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="b38e0-133">Класс main для анализа рукописного ввода — это класс [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="b38e0-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="b38e0-134">При вызове метода [Analyze](/previous-versions/ms568971(v=vs.100)) объекта InkAnalyzer анализ рукописного ввода выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="b38e0-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="b38e0-135">Приложение инициализирует два массива, одну из строк и один из прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="b38e0-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="b38e0-136">Массив строк, состоит `factoidStrings` из объектов [фактоид](/previous-versions/ms583657(v=vs.100)) , которые передаются в [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) как объекты [аналисишинтноде](/previous-versions/ms573018(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="b38e0-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="b38e0-137">Объекты Аналисишинтноде заменяют InkAnalyzer на определенные входные данные.</span><span class="sxs-lookup"><span data-stu-id="b38e0-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="b38e0-138">В этом образце используются Дата, время и телефонные указания, а также другие.</span><span class="sxs-lookup"><span data-stu-id="b38e0-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="b38e0-139">Каждый [аналисишинтноде](/previous-versions/ms573018(v=vs.100)) связан с определенной областью формы.</span><span class="sxs-lookup"><span data-stu-id="b38e0-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="b38e0-140">Области представлены массивом прямоугольников, `rects` .</span><span class="sxs-lookup"><span data-stu-id="b38e0-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="b38e0-141">Создавая [текстовое поле](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) для каждого прямоугольника, образец выводит распознанный текст в нужное расположение.</span><span class="sxs-lookup"><span data-stu-id="b38e0-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



<span data-ttu-id="b38e0-142">После этого создается обработчик событий, который запускает анализ рукописного ввода при нажатии пользователем кнопки анализ.</span><span class="sxs-lookup"><span data-stu-id="b38e0-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
