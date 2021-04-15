---
description: Функции, используемые для перечисления подключенных папок на томе.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Перечисление подключенных папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29585100a4b8a94e1b7b78d36b6f0fda228094d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683699"
---
# <a name="enumerating-mounted-folders"></a>Перечисление подключенных папок

Для перечисления подключенных папок на указанном томе NTFS используются следующие функции.

-   [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**финднекстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**финдволумемаунтпоинтклосе**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Эти функции работают так же, как функции [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)и [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Чтобы перечислить подключенные папки на томе, сначала выясните, поддерживает ли том подключенные папки. Для этого используйте имя тома, возвращенное функциями [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) и [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) , чтобы вызвать функцию [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Возвращаемые имена содержат обратную косую черту ( \) для совместимости с функцией [**жетдриветипе**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) и связанными функциями). Дополнительные сведения о функциях, используемых для проверки томов на компьютере, см. в разделе [перечисление томов](enumerating-volumes.md). При вызове функции **жетволумеинформатион** , если в параметре *ЛПФИЛЕСИСТЕМНАМЕБУФФЕР* возвращается "NTFS", том является томом NTFS. Файловая система NTFS поддерживает подключенные папки.

Если том является томом NTFS, начните поиск подключенных папок, вызвав [**финдфирстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa). Если поиск выполнен успешно, обработайте результаты в соответствии с требованиями приложения. Затем с помощью [**финднекстволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) в цикле найдите и обработайте подключенные папки по одному за раз. Если для перечисления больше нет подключенных папок, закройте маркер поиска, вызвав [**финдволумемаунтпоинтклосе**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose). Обратите внимание, что при поиске будут найдены только подключенные папки на указанном томе.

Не следует рассчитывать на корреляцию между порядком подключенных папок, возвращаемых этими функциями, и порядком подключенных папок, возвращаемых другими функциями или средствами.

 

 



