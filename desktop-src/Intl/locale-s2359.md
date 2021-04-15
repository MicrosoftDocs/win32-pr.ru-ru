---
description: ЯЗЫКовой стандарт \_ S2359 и \_ SPM locale
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 и LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683964"
---
# <a name="locale_s2359-and-locale_spm"></a>ЯЗЫКовой стандарт \_ S2359 и \_ SPM locale

Строка для обозначения PM (второй 12-часовой день). Максимально допустимое число символов для этой строки различается для разных выпусков Windows.

**Windows XP:** Тринадцать, включая завершающий нуль-символ для [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Пятнадцать, включая завершающий нуль-символ для [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

Windows **Me/98/95, Windows NT 4,0, windows 2000:** Девять, включая завершающий нуль-символ.

**Windows Server 2003 и более поздние версии:** Пятнадцать, включая завершающий нуль-символ.

В Windows 10 добавлен параметр **locale \_ SPM** в качестве более удобного синонима для **\_ S2359 локали**.

 

 



