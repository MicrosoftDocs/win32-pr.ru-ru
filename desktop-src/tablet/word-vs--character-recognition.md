---
description: Если для свойства фактоид задано значение None, то распознаватель символов распознает рукописный ввод на основе символьных символов.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Сравнение слов и распознавания символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e704943afb2b411441752056aace0889e87483fc4992d59c39ea6a135ef76b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966603"
---
# <a name="word-vs-character-recognition"></a>Сравнение слов и распознавания символов

Если для свойства [фактоид](/previous-versions/ms835848(v=msdn.10)) задано значение **None**, то распознаватель символов распознает рукописный ввод на основе символьных символов.

Свойство [рекотимеаут](/previous-versions/ms835852(v=msdn.10)) ([**Рекотимеаут**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) в службе автоматизации) определяет время задержки между последним [штрихом](/previous-versions/ms552692(v=vs.100)) и окончанием рукописного ввода в миллисекундах. Это значение можно увеличить, чтобы распознать текст до того, как будут записаны целые слова или предложения. Можно также принудительно выполнить распознавание рукописного ввода с помощью метода [Recognize](/previous-versions/ms836275(v=msdn.10)) .

 

 
