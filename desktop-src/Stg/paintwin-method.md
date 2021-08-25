---
title: Метод Паинтвин
description: Метод Паинтвин
ms.assetid: e89794e6-c059-4531-a1e3-3a4972e0218d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40708700ba4f0175713c59f6e3f1ff1395accadb0dcae3b31ca2e85862a998ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906034"
---
# <a name="paintwin-method"></a>Метод Паинтвин

Ниже приведен метод **Паинтвин** КГУИПАПЕР из гуипапер. CPP.


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



**Паинтвин** по сути вызывает метод **перерисовки** . В примере [стосерве](structured-storage-server-sample--stoserve-.md) метод **перерисовки** был показан для широковещательной рассылки всего массива данных рукописного ввода во все подключенные приемники. **Паинтвин** вызывает объект на стороне сервера для отправки данных рисования клиенту.

 

 




