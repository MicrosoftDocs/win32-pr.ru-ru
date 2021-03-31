---
title: Перенос функций сглаживания
description: Перенос функций сглаживания
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Перенос GL в ГК, сглаживание
- Перенос из ДИАФРАГМы в ГК, сглаживание
- перенос в OpenGL из IRI GL, сглаживание
- Перенос по стандарту OpenGL из IRI GL, сглаживание
- сглаживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411372"
---
# <a name="porting-antialiasing-functions"></a>Перенос функций сглаживания

В OpenGL режим подточки всегда включен, следовательно **, функция IRI** GL (**true**) не требуется и не имеет эквивалента OpenGL. В следующих разделах описаны аспекты переноса кода для сглаживания в ГК.

-   [Перенос кода смешения](porting-blending-code.md)
-   [Перенос тестовых функций афунктион](porting-afunction-test-functions.md)
-   [Использование функций сглаживания](using-antialiasing-functions.md)

 

 




