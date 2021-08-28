---
description: S1159 языкового стандарта \_ и \_ SAM
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 и LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690132c0eb56dc75dd34eae217a6fa7598256852ef4e7039cc988754f7a589f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106344"
---
# <a name="locale_s1159-and-locale_sam"></a>S1159 языкового стандарта \_ и \_ SAM

Строка для обозначения AM (первые 12 часов дня). Максимально допустимое число символов для этой строки, включая завершающий нуль-символ, отличается для разных выпусков Windows.

**Windows XP:** Тринадцать, включая завершающий нуль-символ для [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Пятнадцать, включая завершающий нуль-символ для [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, Windows 2000:** Девять, включая завершающий нуль-символ.

**Windows Server 2003 и более поздних версий:** Пятнадцать, включая завершающий нуль-символ.

Windows 10 добавил значение **\_ SAM locale** в качестве более удобного для чтения синонима для **языкового стандарта \_ S1159**.

 

 



