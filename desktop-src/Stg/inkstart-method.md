---
title: Метод Инкстарт
description: Все методы Инкстарт, Инкдрав и Инкстоп используют конструкции графического пользовательского интерфейса Win32, такие как контексты устройств и объекты пера.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986713"
---
# <a name="inkstart-method"></a><span data-ttu-id="c4e40-103">Метод Инкстарт</span><span class="sxs-lookup"><span data-stu-id="c4e40-103">InkStart Method</span></span>

<span data-ttu-id="c4e40-104">Все методы **инкстарт**, [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) используют конструкции графического пользовательского интерфейса Win32, такие как контексты устройств и объекты пера.</span><span class="sxs-lookup"><span data-stu-id="c4e40-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="c4e40-105">Это иллюстрирует, почему Кгуипапер требуется как отдельный уровень инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="c4e40-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="c4e40-106">Характеристики графического пользовательского интерфейса в графическом документе обрабатываются в Кгуипапер.</span><span class="sxs-lookup"><span data-stu-id="c4e40-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="c4e40-107">Объект собумага отправляет только рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="c4e40-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="c4e40-108">Другой причиной разработки для Кгуипапер уровня инкапсуляции является двойная природа методов **инкстарт**, [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e40-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="c4e40-109">Они не только вызываемы в соотношении для записи рукописных данных по мере их появлении, но и рисуют визуальное изображение рисунка по мере того, как оно происходит.</span><span class="sxs-lookup"><span data-stu-id="c4e40-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="c4e40-110">Кгуипапер сохраняет флаг m \_ бинксавинг для управления этим двойным характером.</span><span class="sxs-lookup"><span data-stu-id="c4e40-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="c4e40-111">Если \_ параметру m бинксавинг присвоено значение false, изображение отображается на экране, но данные не отправляются в бумажную бумагу для записи.</span><span class="sxs-lookup"><span data-stu-id="c4e40-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="c4e40-112">Эта схема используется при перерисовки, когда пользователь не перемещает мышь, а рукописные данные отправляются в Кгуипапер для автоматического перерисовки.</span><span class="sxs-lookup"><span data-stu-id="c4e40-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="c4e40-113">Кгуипапер можно указать, чтобы установить флаг m \_ бинксавинг, вызвав его метод [**инксавинг**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e40-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="c4e40-114">В следующих примерах фрагментов кода показаны методы **инкстарт** объекта гуипапер. CPP И SINK. CPP.</span><span class="sxs-lookup"><span data-stu-id="c4e40-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="c4e40-115">Метод Инкстарт (ГУИПАПЕР. CPP</span><span class="sxs-lookup"><span data-stu-id="c4e40-115">InkStart Method (GUIPAPER.CPP)</span></span>


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="c4e40-116">Метод Инкстарт (SINK. CPP</span><span class="sxs-lookup"><span data-stu-id="c4e40-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="c4e40-117">**Стоклиен** получает данные рисования в форме вызовов подключенного интерфейса **ипаперсинк** в своем объекте копаперсинк.</span><span class="sxs-lookup"><span data-stu-id="c4e40-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="c4e40-118">Эти методы соответствуют аналогичным методам **инкстарт**, [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) в кгуипапер.</span><span class="sxs-lookup"><span data-stu-id="c4e40-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



<span data-ttu-id="c4e40-119">Когда **инкстарт** вызывается в приемнике, он вызывает кгуипапер, чтобы отключить сохранение рукописного ввода в содокументе.</span><span class="sxs-lookup"><span data-stu-id="c4e40-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="c4e40-120">Собумага не требуется получать эхо-копии отправляемых данных.</span><span class="sxs-lookup"><span data-stu-id="c4e40-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="c4e40-121">Когда [**инкдрав**](inkdraw-method.md) вызывается в приемнике, он просто передает вызов в **Кгуипапер:: инкдрав**.</span><span class="sxs-lookup"><span data-stu-id="c4e40-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="c4e40-122">Когда [**инкстоп**](cguipaper-methods.md) вызывается в приемнике, вызывается кгуипапер для включения обратного сохранения рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c4e40-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="c4e40-123">Результатом является воспроизведение данных рукописного ввода собумага в Кгуипапер только для экрана.</span><span class="sxs-lookup"><span data-stu-id="c4e40-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="c4e40-124">Вы можете проверить поведение **стоклиен** при отключении **ипаперсинк** , выбрав в меню приемник пункт Отключить.</span><span class="sxs-lookup"><span data-stu-id="c4e40-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="c4e40-125">В качестве эксперимента после отключения приемника выберите пункт о программе в меню Справка.</span><span class="sxs-lookup"><span data-stu-id="c4e40-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="c4e40-126">Откроется диалоговое окно About (о программе), которое будет охватывать часть рисунка **стоклиен**.</span><span class="sxs-lookup"><span data-stu-id="c4e40-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="c4e40-127">В диалоговом окне о программе нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="c4e40-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="c4e40-128">Обратите внимание, что охваченная часть рисунка теперь исчезла.</span><span class="sxs-lookup"><span data-stu-id="c4e40-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="c4e40-129">Данные рисования не теряются, а часть изображения —.</span><span class="sxs-lookup"><span data-stu-id="c4e40-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="c4e40-130">Клиент получил \_ сообщение WM Paint и выдал метод [**ипапер:: Redraw**](ipaper--redraw.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e40-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="c4e40-131">Но поскольку приемник не был подключен, он не получал вызовы **ипаперсинк** для перерисовки рисования.</span><span class="sxs-lookup"><span data-stu-id="c4e40-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="c4e40-132">Вы также можете проверить это поведение, уменьшив **стоклиен** , а затем восстановив его.</span><span class="sxs-lookup"><span data-stu-id="c4e40-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="c4e40-133">В этом случае все изображение рисунка теряется и нуждается в перерисовки.</span><span class="sxs-lookup"><span data-stu-id="c4e40-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="c4e40-134">Для перерисовки изображения рисунка после выполнения любого из этих тестов используйте меню приемника для повторного подключения, а затем выберите пункт [**перерисовка**](ipaper--redraw.md) в меню рисования.</span><span class="sxs-lookup"><span data-stu-id="c4e40-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




