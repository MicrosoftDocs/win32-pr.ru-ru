---
description: PDH определяет следующие типы данных.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Типы данных счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23208978cfc3c0a67c7547598f26e506a5571a54d0d5ddfc93b7ecff38f9c559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674744"
---
# <a name="performance-counters-data-types"></a>Типы данных счетчиков производительности

## <a name="performance-data-helper-pdh-types"></a>Типы поддержки данных производительности (PDH)

Потребители, использующие функции [модуля поддержки данных производительности (PDH)](using-the-pdh-functions-to-consume-counter-data.md) , используют следующие типы:

| Тип данных | Описание
|-----------|------------
| **PDH \_ хкуери**   | Обработчик запроса. Функция [**пдхопенкуери**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) возвращает этот обработчик. Закройте этот обработчик с помощью [**пдхклосекуери**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **PDH \_ хкаунтер** | Обработчик для счетчика. Функция [**пдхаддкаунтер**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) возвращает этот обработчик. Закройте этот обработчик с помощью [**пдхремовекаунтер**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) или закрыв его в запросе, содержащем счетчик. Не вызывайте **пдхремовекаунтер** для счетчика, если соответствующий запрос уже закрыт. PDH поддерживает связь между счетчиками и запросами и автоматически закрывает дескрипторы счетчиков при закрытии соответствующего дескриптора запроса.
| **PDH \_ HLOG**     | Обработчик файла журнала. Функции [**пдхопенлог**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) и [**пдхбиндинпутдатасаурце**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) возвращают этот обработчик. Закройте этот обработчик с помощью [**пдхклоселог**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **\_состояние PDH**   | Значение состояния PDH. Все функции PDH возвращают значение типа **PDH \_**. Если функция завершается успешно, возвращается значение ошибки \_ Success. В противном случае функция возвращает [код системной ошибки](/windows/desktop/Debug/system-error-codes) или [код ошибки PDH](pdh-error-codes.md).
