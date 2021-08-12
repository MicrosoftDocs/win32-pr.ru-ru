---
description: Шаг 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Шаг 8. Применить изменения свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652060"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



