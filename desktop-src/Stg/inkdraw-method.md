---
title: Метод Инкдрав
description: Кгуипапер также сохраняет флаг m \_ бинкинг. Инкстарт устанавливает значение TRUE, чтобы сообщить о том, что последовательность отрисовки находится в процессе. Например, метод Инкдрав использует этот флаг, чтобы определить, должен ли он рисовать и сохранять рукописные данные.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- инкдрав
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411226"
---
# <a name="inkdraw-method"></a><span data-ttu-id="7d2df-106">Метод Инкдрав</span><span class="sxs-lookup"><span data-stu-id="7d2df-106">InkDraw Method</span></span>

<span data-ttu-id="7d2df-107">Кгуипапер также сохраняет флаг m \_ бинкинг.</span><span class="sxs-lookup"><span data-stu-id="7d2df-107">CGuiPaper also keeps an m\_bInking flag.</span></span> <span data-ttu-id="7d2df-108">[Инкстарт](inkstart-method.md) устанавливает **значение true** , чтобы сообщить о том, что последовательность отрисовки находится в процессе.</span><span class="sxs-lookup"><span data-stu-id="7d2df-108">[InkStart](inkstart-method.md) sets it to **TRUE** to signal that a drawing sequence is in process.</span></span> <span data-ttu-id="7d2df-109">Например, метод Инкдрав использует этот флаг, чтобы определить, должен ли он рисовать и сохранять рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="7d2df-109">For example, the InkDraw method uses this flag to determine whether it should paint and save ink data.</span></span>

<span data-ttu-id="7d2df-110">Ниже приведен метод Инкдрав из ГУИПАПЕР. CPP.</span><span class="sxs-lookup"><span data-stu-id="7d2df-110">The following is the InkDraw method from GUIPAPER.CPP.</span></span>


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



<span data-ttu-id="7d2df-111">Этот метод не выполняет никаких действий \_ , если m бинкинг имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7d2df-111">This method does nothing if m\_bInking is **FALSE**.</span></span> <span data-ttu-id="7d2df-112">Это условие, когда пользователь просто перемещает указатель мыши на окно клиента без нажатия левой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="7d2df-112">This is the condition when the user is simply moving the mouse over the client window without pressing the left mouse button.</span></span>

<span data-ttu-id="7d2df-113">Инкдрав четко имеет две обязанности.</span><span class="sxs-lookup"><span data-stu-id="7d2df-113">InkDraw clearly has a dual responsibility.</span></span> <span data-ttu-id="7d2df-114">Вызовы Win32 Моветоекс и LineTo выполняются для рисования линий изображения на экране графического интерфейса пользователя (с использованием маркера контекста устройства, сохраненного в параметре m \_ HDC).</span><span class="sxs-lookup"><span data-stu-id="7d2df-114">The Win32 MoveToEx and LineTo calls are made to draw line images on the GUI screen (using the device context handle kept in m\_hDC).</span></span> <span data-ttu-id="7d2df-115">Рукописные данные также передаются в объект собумага для записи с помощью метода Инкдрав интерфейса [ипапер](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7d2df-115">The ink data is also passed to the COPaper object for recording using the [IPaper](ipaper-methods.md) interface's InkDraw method.</span></span> <span data-ttu-id="7d2df-116">Если \_ значение m бинксавинг равно **false**, инкдрав закрашивает изображение линии, но не сохраняет данные в составляемой бумаге.</span><span class="sxs-lookup"><span data-stu-id="7d2df-116">When m\_bInkSaving is **FALSE**, InkDraw paints the line image but does not store the data in COPaper.</span></span> <span data-ttu-id="7d2df-117">Это условие используется во время перерисовки.</span><span class="sxs-lookup"><span data-stu-id="7d2df-117">This condition is used during repainting.</span></span>

 

 




