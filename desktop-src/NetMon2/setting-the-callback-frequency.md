---
description: Используйте следующий код, чтобы задать частоту обратного вызова.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Настройка частоты ответного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343865"
---
# <a name="setting-the-callback-frequency"></a>Настройка частоты ответного вызова

Используйте следующий код, чтобы задать частоту обратного вызова:

**Параметр DWORD** Значение = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Этот фрагмент кода задает частоту ответного вызова равным 1 секунде (минимальное значение). Максимальное значение должно быть намного больше 1. Если буфер поставщика сетевых пакетов (НПП) полон, НПП вызывает монитор назад.

 

 



