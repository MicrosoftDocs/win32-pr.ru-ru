---
description: S1159 языкового стандарта \_ и \_ SAM
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 и LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911671"
---
# <a name="locale_s1159-and-locale_sam"></a>S1159 языкового стандарта \_ и \_ SAM

Строка для обозначения AM (первые 12 часов дня). Максимально допустимое число символов для этой строки, включая завершающий нуль-символ, отличается для разных выпусков Windows.

**Windows XP:** Тринадцать, включая завершающий нуль-символ для [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Пятнадцать, включая завершающий нуль-символ для [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

Windows **Me/98/95, Windows NT 4,0, windows 2000:** Девять, включая завершающий нуль-символ.

**Windows Server 2003 и более поздние версии:** Пятнадцать, включая завершающий нуль-символ.

Windows 10 добавил значение **\_ SAM locale** в качестве более удобного для чтения синонима для **языкового стандарта \_ S1159**.

 

 



