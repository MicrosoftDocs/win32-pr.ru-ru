---
description: Описывает, как создать объект Пенинпутпанел.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Создание объекта Пенинпутпанел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692044"
---
# <a name="creating-a-peninputpanel-object"></a>Создание объекта Пенинпутпанел

\[[**Пенинпутпанел**](peninputpanel-class.md) заменен на [**текстинпутпанел**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) и [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)). Дополнительные сведения см. в разделе [Программирование панели ввода текста](programming-the-text-input-panel.md).\]

Конструкторы управляемого кода предоставляют удобный способ создания объекта [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) и его присоединения к элементу управления за один шаг. В этом \# примере на языке C создается объект пенинпутпанел и прикрепляется к существующему элементу управления [InkEdit](/previous-versions/ms835842(v=msdn.10)) `InkEdit1` с одной строкой кода.


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



Тот же пример в Visual Basic .NET выглядит следующим образом:


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



Этот метод полезен в случаях, когда один объект [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) будет связан с одним элементом управления в течение его жизненного цикла. В случаях, когда необходимо использовать один объект Пенинпутпанел и связать его с несколькими элементами управления, как показано в [примере пенинпутпанел](peninputpanel-sample.md), используйте свойство [аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) , чтобы изменить элемент управления, с которым связан объект пенинпутпанел.

Чтобы присоединить объект [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) к элементу управления без использования конструктора, используйте свойство [аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) . Используйте этот метод для языков, которые не поддерживают управляемые конструкторы, такие как C++.

 

 
