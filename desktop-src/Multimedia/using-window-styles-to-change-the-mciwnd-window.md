---
title: Использование стилей окна для изменения окна МЦивнд
description: Использование стилей окна для изменения окна МЦивнд
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Функция МЦивндкреате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661697"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Использование стилей окна для изменения окна МЦивнд

Как и в любом окне, можно изменить внешний вид и поведение окна МЦивнд, выбрав стандартные стили окон, указанные с помощью функции [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Кроме того, можно выбрать один из нескольких других стилей окна, относящихся к МЦивнд окнам. С этими стилями приложение может изменить МЦивнд окна следующими способами:

-   Измените размер окна.
-   Скрытие или отображение элементов управления.
-   Выдача сообщений об уведомлениях.
-   Отображение сведений в заголовке окна.

Стили окна можно задать, указав их в функции [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) , или можно использовать макрос [**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) для изменения стиля существующего окна мЦивнд. Вы также можете запросить окно МЦивнд для его текущих стилей с помощью макроса [**мЦивнджетстилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .

Список стилей окон, относящихся к МЦивнд, см. в разделе [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 