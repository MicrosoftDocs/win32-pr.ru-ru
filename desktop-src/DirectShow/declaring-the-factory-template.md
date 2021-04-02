---
description: Объявление шаблона фабрики
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Объявление шаблона фабрики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139447"
---
# <a name="declaring-the-factory-template"></a>Объявление шаблона фабрики

Следующим шагом является объявление шаблона фабрики для фильтра. Шаблон фабрики — это класс C++, который содержит сведения для фабрики класса. В библиотеке DLL объявите глобальный массив объектов [**кфакторитемплате**](cfactorytemplate.md) , по одному для каждого фильтра или COM-компонента в библиотеке DLL. Массив должен называться *g \_ Templates*. Дополнительные сведения о шаблонах фабрики см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).

Элемент **\_ \_ фильтра m памовиесетуп** шаблона фабрики — это указатель на структуру [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) , описанную ранее. В следующем примере показан шаблон фабрики с использованием структуры, заданной в предыдущем примере.


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



Если вы не объявили какие бы то ни было сведения о фильтре, **m \_ памовесетуп \_ Filter** может иметь **значение NULL**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Как зарегистрировать фильтры DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



