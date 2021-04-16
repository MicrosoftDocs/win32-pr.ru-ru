---
description: Шаг 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Шаг 9. Отключение страницы свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684125"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



