---
description: Позволяет вести мониторинг карт в рамках читателей. Эти подпрограммы обычно используют структуру бросить \_ реадерстате в массиве.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Функции отслеживания смарт-карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912075"
---
# <a name="smart-card-tracking-functions"></a>Функции отслеживания смарт-карт

Следующие функции позволяют отслеживанию карт в рамках читателей. Эти подпрограммы обычно используют структуру [**бросить \_ реадерстате**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) в массиве.



| Раздел                                                | Описание                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**скардлокатекардс**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Поиск карточки, [*строка ATR*](../secgloss/a-gly.md) которой соответствует указанному имени карты. |
| [**скарджетстатусчанже**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Блокировать выполнение до тех пор, пока текущая доступность карт не изменится.                                                                       |
| [**скардканцел**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Завершение невыполненных действий.                                                                                                         |



 

 

 
