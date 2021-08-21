---
description: Шаг 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Шаг 9. Отключение страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf4bcb670b8a8f29334f7ecd41ebba37a915f724be70e5dbbbfd7abea9730be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526085"
---
# <a name="step-9-disconnect-the-property-page"></a>Шаг 9. Отключение страницы свойств

Переопределите метод [**кбасепропертипаже:: ondisconnect**](cbasepropertypage-ondisconnect.md) , чтобы освободить все интерфейсы, полученные в методе **ondisconnect** . Кроме того, если пользователь закрывает страницу свойств без фиксации изменений, следует восстановить исходные значения, если они были изменены. Нет метода "OnCancel", который вызывается при отмене пользователем, поэтому необходимо отследить, что пользователь вызвал **онаппличанжес**. В этом примере используется \_ переменная m лвал, описанная выше.


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



Далее. [Шаг 10. Поддержка регистрации COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



