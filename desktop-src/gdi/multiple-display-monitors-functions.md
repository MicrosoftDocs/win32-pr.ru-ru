---
description: Следующие функции обеспечивают поддержку нескольких мониторов.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Функции нескольких мониторов экрана
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e35ab6fef353f793257721077074271915a3628859471a2f5d89694f6d47440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779144"
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



 

 

 



