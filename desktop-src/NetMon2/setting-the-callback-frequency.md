---
description: Используйте следующий код, чтобы задать частоту обратного вызова.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Настройка частоты ответного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363250"
---
# <a name="setting-the-callback-frequency"></a>Настройка частоты ответного вызова

Используйте следующий код, чтобы задать частоту обратного вызова:

**Параметр DWORD** Значение = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Этот фрагмент кода задает частоту ответного вызова равным 1 секунде (минимальное значение). Максимальное значение должно быть намного больше 1. Если буфер поставщика сетевых пакетов (НПП) полон, НПП вызывает монитор назад.

 

 



