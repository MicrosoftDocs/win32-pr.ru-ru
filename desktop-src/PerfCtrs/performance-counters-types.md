---
description: PDH определяет следующие типы данных.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Типы данных счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663174"
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
