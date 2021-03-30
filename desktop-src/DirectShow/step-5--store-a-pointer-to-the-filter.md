---
description: Шаг 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Шаг 5. Сохранение указателя на фильтр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265960"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Шаг 5. Сохранение указателя на фильтр

Переопределите метод [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) , чтобы сохранить указатель на фильтр. В следующем примере запрашивается параметр *Punk* для пользовательского интерфейса исатуратион фильтра:


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



Далее. [Шаг 6. Инициализируйте диалоговое окно](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



