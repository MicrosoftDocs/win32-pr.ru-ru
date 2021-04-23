---
title: Пример кода рендеринга
description: Пример кода рендеринга
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- визуализации, пример кода
- Пользовательские визуализации, пример кода
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- Функция Render, пример кода
- Примеры, функция Render для визуализаций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068216"
---
# <a name="sample-render-code"></a><span data-ttu-id="d6387-109">Пример кода рендеринга</span><span class="sxs-lookup"><span data-stu-id="d6387-109">Sample Render Code</span></span>

<span data-ttu-id="d6387-110">Ниже приведен пример кода, который использует функцию **Render** для рисования линии на экране.</span><span class="sxs-lookup"><span data-stu-id="d6387-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="d6387-111">Высота линии определяется значением волны.</span><span class="sxs-lookup"><span data-stu-id="d6387-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="d6387-112">Функция **Render** — это место, где происходит основная работа кода.</span><span class="sxs-lookup"><span data-stu-id="d6387-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="d6387-113">Каждый раз, когда проигрыватель Windows Media создает моментальный снимок звука, он вызывает эту функцию, и код будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="d6387-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="d6387-114">Этот код выполняет следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="d6387-114">This code performs the following tasks.</span></span> <span data-ttu-id="d6387-115">Дополнительные сведения о конкретных функциях см. в разделе пакет SDK для платформы Microsoft Windows для 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="d6387-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="d6387-116">Создание объектов</span><span class="sxs-lookup"><span data-stu-id="d6387-116">Creating Objects</span></span>

<span data-ttu-id="d6387-117">Обычно используются функции рисования, которые входят в состав графического интерфейса Microsoft Windows (GDI).</span><span class="sxs-lookup"><span data-stu-id="d6387-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="d6387-118">Необходимо создать перья для рисования линий и кистей для заполнения областей.</span><span class="sxs-lookup"><span data-stu-id="d6387-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="d6387-119">Для заполнения фона создается сплошная черная кисть.</span><span class="sxs-lookup"><span data-stu-id="d6387-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="d6387-120">Для рисования линии создается сплошное перо.</span><span class="sxs-lookup"><span data-stu-id="d6387-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="d6387-121">Цвет будет основным цветом, определяемым обложкой, которая будет отображать визуализацию.</span><span class="sxs-lookup"><span data-stu-id="d6387-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="d6387-122">Добавление объекта в контроллер домена</span><span class="sxs-lookup"><span data-stu-id="d6387-122">Adding the Object to the DC</span></span>

<span data-ttu-id="d6387-123">Необходимо добавить перо в контекст устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="d6387-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="d6387-124">Контроллер домена — это часть памяти, в которой хранятся все данные и объекты рисования.</span><span class="sxs-lookup"><span data-stu-id="d6387-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="d6387-125">По сути, контроллер домена — это окно диспетчера трафика, которое отслеживает все графические изображения.</span><span class="sxs-lookup"><span data-stu-id="d6387-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="d6387-126">Необходимо *привести* созданный объект Pen и сохранить его как старое перо.</span><span class="sxs-lookup"><span data-stu-id="d6387-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="d6387-127">Используйте этот прием кодирования для всех новых перьев.</span><span class="sxs-lookup"><span data-stu-id="d6387-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="d6387-128">Этот метод необходим для 32-разрядного программирования.</span><span class="sxs-lookup"><span data-stu-id="d6387-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="d6387-129">Заполнение фона</span><span class="sxs-lookup"><span data-stu-id="d6387-129">Filling in the Background</span></span>

<span data-ttu-id="d6387-130">Теперь все готово для рисования.</span><span class="sxs-lookup"><span data-stu-id="d6387-130">You now are ready to draw.</span></span> <span data-ttu-id="d6387-131">Функция **филлрект** будет заполнять прямоугольник окна, как определено параметрами функции **Render** .</span><span class="sxs-lookup"><span data-stu-id="d6387-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="d6387-132">Прямоугольник заполняется черной кистью.</span><span class="sxs-lookup"><span data-stu-id="d6387-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="d6387-133">Получение звуковых данных</span><span class="sxs-lookup"><span data-stu-id="d6387-133">Getting Audio Data</span></span>

<span data-ttu-id="d6387-134">Далее код получает некоторые звуковые данные из проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d6387-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="d6387-135">Используя массив форм, можно получить текущее значение звукового сигнала в момент создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d6387-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="d6387-136">В этом случае вы принимаете звуковые данные левого канала.</span><span class="sxs-lookup"><span data-stu-id="d6387-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="d6387-137">Первое значение в массиве является первым 1024thом снимка состояния звука.</span><span class="sxs-lookup"><span data-stu-id="d6387-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="d6387-138">Эти сведения будут использоваться для вывода строки, высота которой будет соответствовать снимку энергии звука.</span><span class="sxs-lookup"><span data-stu-id="d6387-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="d6387-139">Рисование линии</span><span class="sxs-lookup"><span data-stu-id="d6387-139">Draw the Line</span></span>

<span data-ttu-id="d6387-140">Линия рисуется слева направо с помощью функций GDI **моветоекс** и **lineTo** .</span><span class="sxs-lookup"><span data-stu-id="d6387-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="d6387-141">Сначала переместите перо на начальную точку.</span><span class="sxs-lookup"><span data-stu-id="d6387-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="d6387-142">В этом случае x и y используются для определения значений слева направо и сверху вниз, которые пользователь увидит на экране.</span><span class="sxs-lookup"><span data-stu-id="d6387-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="d6387-143">X определяется прямоугольником PRC и, в частности, значением КНР->Left.</span><span class="sxs-lookup"><span data-stu-id="d6387-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="d6387-144">Y определяется как значение данных волны в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d6387-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="d6387-145">Затем вы рисуете линию на другой стороне окна.</span><span class="sxs-lookup"><span data-stu-id="d6387-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="d6387-146">Точка, в которую рисуется линия, снова будет иметь значение x, y.</span><span class="sxs-lookup"><span data-stu-id="d6387-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="d6387-147">X определяется прямоугольником PRC, но на этот раз — PRC->right.</span><span class="sxs-lookup"><span data-stu-id="d6387-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="d6387-148">Y по-прежнему определяется данными волны и совпадает с точкой, с которой вы начали, так как вы рисуете прямую линию слева направо.</span><span class="sxs-lookup"><span data-stu-id="d6387-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="d6387-149">Очистить все</span><span class="sxs-lookup"><span data-stu-id="d6387-149">Clean up Everything</span></span>

<span data-ttu-id="d6387-150">Необходимо удалить созданные объекты.</span><span class="sxs-lookup"><span data-stu-id="d6387-150">You must delete the objects you create.</span></span> <span data-ttu-id="d6387-151">В частности, необходимо удалить все созданные кисти и перья.</span><span class="sxs-lookup"><span data-stu-id="d6387-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="d6387-152">При завершении работы с ними рекомендуется удалить перья и кисти.</span><span class="sxs-lookup"><span data-stu-id="d6387-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="d6387-153">Если вы не удалите их перед завершением реализации функции **Render** , Визуализация будет завершаться сбоем в течение минуты или меньше.</span><span class="sxs-lookup"><span data-stu-id="d6387-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="d6387-154">Необходимо сосчитать число перьев и кистей и уничтожить каждое из них.</span><span class="sxs-lookup"><span data-stu-id="d6387-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="d6387-155">Будьте внимательны, чтобы не создавать перья внутри цикла кода.</span><span class="sxs-lookup"><span data-stu-id="d6387-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="d6387-156">Используйте методику кодирования, приведенную в примере, чтобы уничтожить перья и кисти.</span><span class="sxs-lookup"><span data-stu-id="d6387-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="d6387-157">**Важно!** Удалите перья и кисти!</span><span class="sxs-lookup"><span data-stu-id="d6387-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="d6387-158">Когда вы завершите очистку, не забудьте вернуть S \_ OK, чтобы проигрыватель Windows Media знал, что вы закончили рисовать.</span><span class="sxs-lookup"><span data-stu-id="d6387-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="d6387-159">После того, как вы закончите, ваш рисунок будет передан в окно, будет создан другой моментальный **снимок, после этого будет выдан** запрос на прорисовку кода и т. д.</span><span class="sxs-lookup"><span data-stu-id="d6387-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6387-160">См. также</span><span class="sxs-lookup"><span data-stu-id="d6387-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6387-161">**Реализация отрисовки**</span><span class="sxs-lookup"><span data-stu-id="d6387-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




