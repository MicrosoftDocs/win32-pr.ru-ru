---
title: Метод Паинтвин
description: Метод Паинтвин
ms.assetid: e89794e6-c059-4531-a1e3-3a4972e0218d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b30e7a52640255934762943f910e367d76088d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332744"
---
# <a name="paintwin-method"></a><span data-ttu-id="48388-103">Метод Паинтвин</span><span class="sxs-lookup"><span data-stu-id="48388-103">PaintWin Method</span></span>

<span data-ttu-id="48388-104">Ниже приведен метод **Паинтвин** КГУИПАПЕР из гуипапер. CPP.</span><span class="sxs-lookup"><span data-stu-id="48388-104">The following is CGuiPaper's **PaintWin** method from GUIPAPER.CPP.</span></span>


```C++
HRESULT CGuiPaper::PaintWin(void)
  {
    HRESULT hr = E_FAIL;
    COLORREF crInkColor;
    SHORT nInkWidth;

    if (m_pIPaper && !m_bPainting && !m_bInking)
    {
      m_bPainting = TRUE;
      // Save and restore ink color and width since redraw otherwise
      // ends up changing these values in CGuiPaper.
      crInkColor = m_crInkColor;
      nInkWidth = m_nInkWidth;
      hr = m_pIPaper->Redraw(m_nLockKey);
      m_nInkWidth = nInkWidth;
      m_crInkColor = crInkColor;
      m_bPainting = FALSE;
    }

    return hr;
  }
```



<span data-ttu-id="48388-105">**Паинтвин** по сути вызывает метод **перерисовки** .</span><span class="sxs-lookup"><span data-stu-id="48388-105">**PaintWin** essentially calls COPaper's **Redraw** method.</span></span> <span data-ttu-id="48388-106">В примере [стосерве](structured-storage-server-sample--stoserve-.md) метод **перерисовки** был показан для широковещательной рассылки всего массива данных рукописного ввода во все подключенные приемники.</span><span class="sxs-lookup"><span data-stu-id="48388-106">In the [StoServe](structured-storage-server-sample--stoserve-.md) sample, the **Redraw** method was shown to broadcast COPaper's entire ink data array to all connected sinks.</span></span> <span data-ttu-id="48388-107">**Паинтвин** вызывает объект на стороне сервера для отправки данных рисования клиенту.</span><span class="sxs-lookup"><span data-stu-id="48388-107">**PaintWin** calls an object on the server side to send back the drawing data to the client.</span></span>

 

 




