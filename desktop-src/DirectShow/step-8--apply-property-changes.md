---
description: Шаг 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Шаг 8. Применить изменения свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674170"
---
# <a name="step-8-apply-property-changes"></a>Шаг 8. Применить изменения свойств

Переопределите метод [**кбасепропертипаже:: онаппличанжес**](cbasepropertypage-onapplychanges.md) , чтобы зафиксировать изменения свойств. В этом примере \_ переменная m лневвал обновляется всякий раз, когда пользователь прокручивает ползунок. Метод **онаппличанжес** копирует это значение в \_ переменную m лвал, перезаписывая исходное значение:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Далее. [Шаг 9. Отключение страницы свойств](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



