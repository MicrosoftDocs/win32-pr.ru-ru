---
description: В этом образце показано, как использовать анализ рукописного ввода для создания приложения заполнения форм, в котором форма основана на отсканированной бумажной форме.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Бумажная форма анализа рукописного текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718650"
---
# <a name="ink-analysis-scanned-paper-form"></a>Бумажная форма анализа рукописного текста

В этом образце показано, как использовать анализ рукописного ввода для создания приложения заполнения форм, в котором форма основана на отсканированной бумажной форме.

## <a name="features-demonstrated"></a>Демонстрируемые возможности

в этом примере приложения демонстрируются следующие возможности API анализа рукописного ввода и Windows Forms элементов управления рукописного ввода:

-   Загрузка печатной формы. В этом примере форма импортируется из изображения в формате .png.
-   Сбор и отрисовка рукописного ввода поверх сканируемой формы.
-   Использование объекта [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) для анализа рукописного текста.
-   Создание объектов [аналисишинтноде](/previous-versions/ms573018(v=vs.100)) для улучшения результатов рукописного ввода.
-   Заполнение текстовых полей в подсказках анализа.
-   Создание базовой работы по исправлению текста.

## <a name="project-references"></a>Ссылки проекта

пример доступен в виде приложения Windows Forms или Windows Presentation Foundation. ссылки на Windows Forms версии:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

версия Windows Presentation Foundation ссылается на IAWinFX.dll в дополнение к основным Windows Presentation Foundation библиотекам dll.

> [!Note]  
> для Windows Presentation Foundation версии этого образца (найден в каталоге XAML) требуется, чтобы в системе были установлены расширения Windows Presentation Foundation для Microsoft Visual Studio 2005.

 

## <a name="user-interface"></a>Пользовательский интерфейс

Пользовательский интерфейс для этого приложения состоит из элемента [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) с двумя связанными объектами [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) : рукописная форма и преобразованная Текстовая форма. Вкладка форма рукописного ввода содержит

-   Панель, содержащая изображение печатной формы, используемой для получения телефонных сообщений.
-   Флажок, имеющий приложение, отображает границы подсказок анализа при выборе.
-   Пара кнопок, очищает и анализирует, которые очищают рукописный ввод из формы и инициализируют анализ рукописного ввода.

Преобразованная Текстовая форма содержит то же изображение, а — страницу, на которой приложение отображает распознанный текст. При нажатии кнопки анализ приложение выполняет анализ рукописного ввода в синхронном режиме, а результаты распознавания отображаются на вкладке преобразованная Текстовая форма.

## <a name="functionality"></a>функциональное назначение;

Это приложение использует [InkOverlay](/previous-versions/ms552322(v=vs.100)) для включения записи. Объект InkOverlay хорошо подходит для создания заметок и создания базовых кривых. Основным предполагаемым использованием этого объекта является отображение рукописных данных в виде рукописных данных. Класс main для анализа рукописного ввода — это класс [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) . При вызове метода [Analyze](/previous-versions/ms568971(v=vs.100)) объекта InkAnalyzer анализ рукописного ввода выполняется синхронно.

Приложение инициализирует два массива, одну из строк и один из прямоугольников. Массив строк, состоит `factoidStrings` из объектов [фактоид](/previous-versions/ms583657(v=vs.100)) , которые передаются в [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) как объекты [аналисишинтноде](/previous-versions/ms573018(v=vs.100)) . Объекты Аналисишинтноде заменяют InkAnalyzer на определенные входные данные. В этом образце используются Дата, время и телефонные указания, а также другие.

Каждый [аналисишинтноде](/previous-versions/ms573018(v=vs.100)) связан с определенной областью формы. Области представлены массивом прямоугольников, `rects` . Создавая [текстовое поле](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) для каждого прямоугольника, образец выводит распознанный текст в нужное расположение.


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



После этого создается обработчик событий, который запускает анализ рукописного ввода при нажатии пользователем кнопки анализ.


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



 

 
