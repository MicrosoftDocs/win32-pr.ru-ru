---
description: После создания обработчика для INF-файла можно получить сведения из него различными способами. Такие функции, как Сетупжетинфинформатион, Сетупкуеринффилеинформатион и Сетупкуеринфверсионинформатион, извлекают сведения о самом INF-файле.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Получение сведений из INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663423"
---
# <a name="retrieving-information-from-an-inf-file"></a>Получение сведений из INF-файла

После создания обработчика для INF-файла можно получить сведения из него различными способами. Такие функции, как [**сетупжетинфинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**сетупкуеринффилеинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)и [**сетупкуеринфверсионинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) , извлекают сведения о самом INF-файле.

Другие функции, такие как [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) и [**сетупжеттаржетпас**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , получают сведения о исходных файлах и целевых каталогах.

Низкоуровневые функции, такие как [**сетупжетлинетекст**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) и [**сетупжетстрингфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) , позволяют напрямую обращаться к информации, хранящейся в строке или поле INF-файла. Эти функции используются внутренне функциями более высокого уровня, но также доступны для доступа к информации INF на уровне строки или поля.

 

 



