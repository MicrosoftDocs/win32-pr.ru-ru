---
description: ЯЗЫКовой стандарт \_ S2359 и \_ SPM locale
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 и LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8690d40907135b88966286c8cb36cf72cf31f372ba2160fc6d49637ac813129d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106324"
---
# <a name="locale_s2359-and-locale_spm"></a>ЯЗЫКовой стандарт \_ S2359 и \_ SPM locale

Строка для обозначения PM (второй 12-часовой день). Максимально допустимое число символов для этой строки различается для разных выпусков Windows.

**Windows XP:** Тринадцать, включая завершающий нуль-символ для [**сетлокалеинфо**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Пятнадцать, включая завершающий нуль-символ для [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, Windows 2000:** Девять, включая завершающий нуль-символ.

**Windows Server 2003 и более поздних версий:** Пятнадцать, включая завершающий нуль-символ.

Windows 10 добавил значение **LOCALE \_ SPM** в качестве более удобного синонима **для \_ S2359 локали**.

 

 



