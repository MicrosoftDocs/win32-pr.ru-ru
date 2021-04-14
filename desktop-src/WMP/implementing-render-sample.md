---
title: Реализация образца рендеринга
description: Реализация образца рендеринга
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- визуализации, пример с свечением
- Пользовательские визуализации, пример свечения
- инструкции по программированию, визуализации
- Примеры, Визуализация свечения
- Пример визуализации с свечением
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- Функция Render, пример свечения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533716"
---
# <a name="implementing-render-sample"></a><span data-ttu-id="88bac-111">Реализация образца рендеринга</span><span class="sxs-lookup"><span data-stu-id="88bac-111">Implementing Render Sample</span></span>

<span data-ttu-id="88bac-112">Следующий код используется для реализации функции **Render** :</span><span class="sxs-lookup"><span data-stu-id="88bac-112">The following code is used to implement the **Render** function:</span></span>


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



<span data-ttu-id="88bac-113">Ниже приведено описание кода.</span><span class="sxs-lookup"><span data-stu-id="88bac-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="88bac-114">Переменная с именем *миколор* используется для цвета свечения и объявляется с помощью **COLORREF**.</span><span class="sxs-lookup"><span data-stu-id="88bac-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="88bac-115">Все цвета должны использовать тип данных **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="88bac-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="88bac-116">Для моментального снимка уровня звуковой волны используется переменная с именем *милевел* .</span><span class="sxs-lookup"><span data-stu-id="88bac-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="88bac-117">Это значение будет зависеть от фактического уровня потребления на момент создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="88bac-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="88bac-118">Оператор **switch** задается предустановкой, которую пользователь выбрал в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="88bac-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="88bac-119">При выборе будет задан желаемый цвет *миколор* (красный, зеленый или синий).</span><span class="sxs-lookup"><span data-stu-id="88bac-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="88bac-120">Однако точный цвет будет определяться уровнем громкости звука.</span><span class="sxs-lookup"><span data-stu-id="88bac-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="88bac-121">Например, если выбрана Красная предустановка, цвет будет сплошным красным, но он будет светлее или темнее в зависимости от звуковой волны в момент создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="88bac-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="88bac-122">Чтобы создать свой цвет, обязательно используйте макрос **РБГ** .</span><span class="sxs-lookup"><span data-stu-id="88bac-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="88bac-123">Создается кисть с именем *хневбруш*, которая используется для заполнения прямоугольника *PRC* , предоставляемого проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="88bac-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="88bac-124">Поверхность рисования — это контекст устройства *HDC* , предоставляемый проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="88bac-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="88bac-125">Кисть удаляется с помощью **DeleteObject**.</span><span class="sxs-lookup"><span data-stu-id="88bac-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="88bac-126">Обязательно удалите все созданные вами перья или кисти.</span><span class="sxs-lookup"><span data-stu-id="88bac-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="88bac-127">После завершения кода **рендеринга** проигрыватель Windows Media *отобразит графическое окно в окне,* определяемом используемой обложкой.</span><span class="sxs-lookup"><span data-stu-id="88bac-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88bac-128">См. также</span><span class="sxs-lookup"><span data-stu-id="88bac-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88bac-129">**Пример свечения**</span><span class="sxs-lookup"><span data-stu-id="88bac-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




