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
# <a name="inkstart-method"></a>Метод Инкстарт

Все методы **инкстарт**, [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) используют конструкции графического пользовательского интерфейса Win32, такие как контексты устройств и объекты пера. Это иллюстрирует, почему Кгуипапер требуется как отдельный уровень инкапсуляции. Характеристики графического пользовательского интерфейса в графическом документе обрабатываются в Кгуипапер. Объект собумага отправляет только рукописные данные.

Другой причиной разработки для Кгуипапер уровня инкапсуляции является двойная природа методов **инкстарт**, [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) . Они не только вызываемы в соотношении для записи рукописных данных по мере их появлении, но и рисуют визуальное изображение рисунка по мере того, как оно происходит. Кгуипапер сохраняет флаг m \_ бинксавинг для управления этим двойным характером. Если \_ параметру m бинксавинг присвоено значение false, изображение отображается на экране, но данные не отправляются в бумажную бумагу для записи.

Эта схема используется при перерисовки, когда пользователь не перемещает мышь, а рукописные данные отправляются в Кгуипапер для автоматического перерисовки. Кгуипапер можно указать, чтобы установить флаг m \_ бинксавинг, вызвав его метод [**инксавинг**](cguipaper-methods.md) .

В следующих примерах фрагментов кода показаны методы **инкстарт** объекта гуипапер. CPP И SINK. CPP.

## <a name="inkstart-method-guipapercpp"></a>Метод Инкстарт (ГУИПАПЕР. CPP


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



## <a name="inkstart-method-sinkcpp"></a>Метод Инкстарт (SINK. CPP

**Стоклиен** получает данные рисования в форме вызовов подключенного интерфейса **ипаперсинк** в своем объекте копаперсинк. Эти методы соответствуют аналогичным методам **инкстарт**, [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) в кгуипапер.


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



Когда **инкстарт** вызывается в приемнике, он вызывает кгуипапер, чтобы отключить сохранение рукописного ввода в содокументе. Собумага не требуется получать эхо-копии отправляемых данных. Когда [**инкдрав**](inkdraw-method.md) вызывается в приемнике, он просто передает вызов в **Кгуипапер:: инкдрав**. Когда [**инкстоп**](cguipaper-methods.md) вызывается в приемнике, вызывается кгуипапер для включения обратного сохранения рукописного ввода. Результатом является воспроизведение данных рукописного ввода собумага в Кгуипапер только для экрана.

Вы можете проверить поведение **стоклиен** при отключении **ипаперсинк** , выбрав в меню приемник пункт Отключить. В качестве эксперимента после отключения приемника выберите пункт о программе в меню Справка. Откроется диалоговое окно About (о программе), которое будет охватывать часть рисунка **стоклиен**. В диалоговом окне о программе нажмите кнопку ОК. Обратите внимание, что охваченная часть рисунка теперь исчезла. Данные рисования не теряются, а часть изображения —. Клиент получил \_ сообщение WM Paint и выдал метод [**ипапер:: Redraw**](ipaper--redraw.md) . Но поскольку приемник не был подключен, он не получал вызовы **ипаперсинк** для перерисовки рисования.

Вы также можете проверить это поведение, уменьшив **стоклиен** , а затем восстановив его. В этом случае все изображение рисунка теряется и нуждается в перерисовки. Для перерисовки изображения рисунка после выполнения любого из этих тестов используйте меню приемника для повторного подключения, а затем выберите пункт [**перерисовка**](ipaper--redraw.md) в меню рисования.

 

 




