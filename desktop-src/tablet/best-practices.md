---
description: Общие сведения о рекомендациях при использовании объекта панели ввода пера.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Рекомендации (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272844"
---
# <a name="best-practices-tablet-pc"></a>Рекомендации (планшетный ПК)

При использовании объекта [**пенинпутпанел**](peninputpanel-class.md) необходимо учитывать несколько рекомендаций.

-   [Предпочитать элемент управления InkEdit](#prefer-inkedit-control)
-   [Отключение режима рукописного ввода для элементов управления InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Использование безоконных элементов управления](#using-windowless-controls)
-   [См. также](#related-topics)

## <a name="prefer-inkedit-control"></a>Предпочитать элемент управления InkEdit

[InkEdit](inkedit-control-reference.md) — предпочтительный элемент управления для присоединения объекта [**пенинпутпанел**](peninputpanel-class.md) . Элемент управления InkEdit обеспечивает поддержку [платформы текстовых служб (TSF)](text-services-framework.md).

## <a name="disable-ink-mode-on-inkedit-controls"></a>Отключение режима рукописного ввода для элементов управления InkEdit

При присоединении к элементу управления [InkEdit](inkedit-control-reference.md) присвойте свойству [**Инкмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) элемента управления InkEdit значение [**инкмоде**](/windows/desktop/api/inked/ne-inked-inkmode) . Если для свойства **инкмоде** не задано значение **инкмоде** , то элемент управления InkEdit интерпретирует первое касание как росчерк, передает его распознавателю и вставляет текст в элемент управления InkEdit. Так как у вас уже есть объект [**пенинпутпанел**](peninputpanel-class.md) , присоединенный к приему рукописного ввода, нет необходимости включать элемент управления InkEdit для рукописного ввода.

## <a name="using-windowless-controls"></a>Использование безоконных элементов управления

Когда объект [**пенинпутпанел**](peninputpanel-class.md) присоединяется к родительскому окну, содержащему более одного безоконного элемента управления, объект **пенинпутпанел** не знает, как отвести курсор в фокусе между дочерними окнами. Рукописный ввод может отправляться неправильному дочернему элементу, когда фокус перемещается из одного безоконного элемента управления в другой в ожидании ввода.

Чтобы использовать объект [**пенинпутпанел**](peninputpanel-class.md) в безоконной среде, можно использовать следующий метод:

1.  Создайте экземпляр элемента управления [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) и поместите его в безоконный элемент управления.
2.  Присоедините объект [**пенинпутпанел**](peninputpanel-class.md) к новому элементу управления "текстовое поле".
3.  Пусть элемент управления "текстовое поле" соберет распознанный текст из объекта [**пенинпутпанел**](peninputpanel-class.md) .
4.  При изменении фокуса с элемента управления "текстовое поле" вызовите метод [**коммитпендингинпут**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) объекта [**пенинпутпанел**](peninputpanel-class.md) .
5.  Скопируйте распознанный текст из элемента управления "текстовое поле" в неоконное дочернее окно.
6.  Отсоедините объект [**пенинпутпанел**](peninputpanel-class.md) , задав свойству [аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) (только управляемый код) или свойства [**аттачедедитвиндов**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) значение null.
7.  Уничтожить элемент управления "текстовое поле".

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Класс Пенинпутпанел**](peninputpanel-class.md)
</dt> <dt>

[Microsoft. Ink. Пенинпутпанел](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[инфраструктуры текстовых служб (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 
