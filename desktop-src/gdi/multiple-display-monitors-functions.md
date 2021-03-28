---
description: Следующие функции обеспечивают поддержку нескольких мониторов.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Функции нескольких мониторов экрана
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984928"
---
# <a name="multiple-display-monitors-functions"></a>Функции нескольких мониторов экрана

Следующие функции обеспечивают поддержку нескольких мониторов.



| Функция                                           | Описание                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Перечисляет мониторы, пересекающие регион, образованный пересечением указанного прямоугольника обрезки и видимой области контекста устройства. |
| [**жетмониторинфо**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Извлекает сведения о мониторе отображения.                                                                                                               |
| [**мониторенумпрок**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Определяемая приложением функция обратного вызова, вызываемая функцией [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .                                  |
| [**мониторфромпоинт**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Извлекает маркер монитора, который содержит указанную точку.                                                                                   |
| [**мониторфромрект**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Извлекает маркер монитора, который имеет большую часть пересечения с указанным прямоугольником.                                              |
| [**мониторфромвиндов**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Извлекает маркер монитора, который имеет большую часть пересечения с ограничивающим прямоугольником заданного окна.                       |



 

 

 



