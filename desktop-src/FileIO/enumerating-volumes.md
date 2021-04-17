---
description: Чтобы создать полный список томов на компьютере или управлять каждым томом, можно перечислить тома.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Перечисление томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683700"
---
# <a name="enumerating-volumes"></a>Перечисление томов

Чтобы создать полный список томов на компьютере или управлять каждым томом, можно перечислить тома. В томе можно [проверить наличие подключенных папок](enumerating-volume-mount-points.md) или других объектов в томе.

Три функции позволяют приложению перечислять тома на компьютере:

-   [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**финдволумеклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

Эти три функции работают так же, как функции [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)и [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Начните поиск томов с помощью [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew). Если поиск прошел успешно, обработайте результаты в соответствии со структурой приложения. Затем используйте [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) в цикле для нахождения и обработки каждого последующего тома. Когда предоставление томов будет исчерпано, закройте Поиск с помощью [**финдволумеклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).

Не следует рассчитывать на корреляцию между порядком томов, возвращаемых этими функциями, и порядком томов, возвращаемых другими функциями или инструментами. В частности, не следует рассчитывать на корреляцию между порядком использования томов и буквами дисков, назначенными BIOS (при наличии) или администратором дисков.

Пример перечисления томов на компьютере см. в разделе [примеры подключенной папки](volume-mount-point-examples.md) .

 

 



