---
description: Сохранение указателя на фильтр в рамках создания страницы свойств фильтра для настраиваемого фильтра DirectShow.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Шаг 5. Сохранение указателя на фильтр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406797"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



