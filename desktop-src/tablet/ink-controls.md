---
description: Обзор элементов управления рукописным вводом для планшетных ПК.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Элементы управления рукописным вводом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541314"
---
# <a name="ink-controls"></a>Элементы управления рукописным вводом

Платформа Tablet PC предоставляет два элемента управления: [InkEdit](inkedit-control.md) и [InkPicture](inkpicture-control.md), которые позволяют легко добавлять рукописные данные и распознавание рукописного ввода в приложения для планшетных ПК. Элемент управления InkEdit имеет версии [Managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) и Win32, в то время как InkPicture имеет только управляемые версии [InkPicture](/previous-versions/ms583740(v=vs.100)) и [ActiveX](inkpicture-control-reference.md) .

Основное различие между элементами управления заключается в том, как сохраняются данные. Элемент управления [InkEdit](inkedit-control.md) сохраняет рукописные данные в виде текста по умолчанию, а в процессе [InkPicture](inkpicture-control.md) рукописный ввод сохраняется.

Элемент управления [InkEdit](inkedit-control.md) предназначен для ввода текста с помощью распознавания рукописного ввода. [InkPicture](inkpicture-control.md) предназначен для аннотации (например, при пометке слайда презентации или другого изображения).

В управляемом коде создайте элементы управления рукописным вводом в том же потоке, что и основной поток для формы. Если элемент управления [InkEdit](inkedit-control.md) или [InkPicture](inkpicture-control.md) создается в другом потоке, приложение может не реагировать должным образом.

Перед созданием элемента управления рукописного ввода необходимо явно изменить модель потоков на подразделение с одним потоком (STA). Это приводит к тому, что элемент управления создается в основном потоке. Для явной установки потоковой модели можно использовать следующий управляемый код C++.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Для того же результата в C можно использовать следующий код \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Чтобы избежать утечки памяти в управляемом коде, необходимо явным образом вызвать метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) на любом элементе управления Tablet PC, к которому был присоединен обработчик событий, прежде чем элемент управления выходит из области действия.

В следующих разделах описываются элементы управления рукописного ввода и использование элементов управления рукописного ввода в приложениях.

-   [Добавление элементов управления рукописного ввода в проект](adding-ink-controls-to-a-project.md)
-   [Элемент управления InkEdit](inkedit-control.md)
-   [Элемент управления InkPicture](inkpicture-control.md)

 

 
