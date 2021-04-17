---
description: Работа с меню DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Работа с меню DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684710"
---
# <a name="working-with-dvd-menus"></a>Работа с меню DVD

Навигатор DVD может показывать меню, когда пользователь активирует кнопку или когда навигатор входит в первый домен воспроизведения. Чтобы отобразить меню программным способом, вызовите метод [**IDvdControl2:: шовмену**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .

Существует несколько способов выбора кнопок меню программным способом.

-   Чтобы выбрать кнопку по номеру, вызовите [**IDvdControl2:: селектбуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). Номера кнопок нумеруются от 1 до 36. Метод [**IDvdInfo2:: жеткуррентбуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) возвращает количество доступных кнопок.
-   Чтобы выбрать кнопку относительно положения выбранной в данный момент кнопки, вызовите метод [**IDvdControl2:: селектрелативебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). Можно выбрать кнопку в направлении вверх, вниз, влево или вправо.
-   Чтобы выбрать кнопку по ее координатам в окне, вызовите [**IDvdControl2:: селектатпоситион**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Этот метод принимает координаты (x, y) относительно клиентской области окна видео. (Для режима без окон это окно приложения.) Если в этом месте нет кнопки, метод возвращает \_ кнопку VFW E \_ DVD \_ No (нет) \_ .

Кроме того, существует несколько способов активации кнопки:

-   Чтобы активировать кнопку по номеру, вызовите [**IDvdControl2:: селектандактиватебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).
-   Чтобы активировать кнопку по ее координатам, вызовите [**IDvdControl2:: активатеатпоситион**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).
-   Чтобы активировать кнопку, которая в данный момент выбрана, вызовите метод [**IDvdControl2:: активатебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Если кнопка не выбрана, метод возвращает кнопку VFW \_ E \_ DVD \_ No \_ (нет).

Помните, что при выборе кнопки просто выделяются ее границы. Чтобы запустить связанную команду, необходимо активировать кнопку. Программная активация кнопки может выполняться различными способами, но перед активацией эту кнопку всегда нужно выбрать.

## <a name="related-topics"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 



