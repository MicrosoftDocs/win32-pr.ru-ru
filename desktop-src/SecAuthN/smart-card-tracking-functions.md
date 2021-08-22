---
description: Позволяет вести мониторинг карт в рамках читателей. Эти подпрограммы обычно используют структуру бросить \_ реадерстате в массиве.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Функции отслеживания смарт-карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b81ce357cf683d29c1a86d48993c16b7f363635b8e6e3c7e0f2a6ad0900f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917344"
---
# <a name="smart-card-tracking-functions"></a>Функции отслеживания смарт-карт

Следующие функции позволяют отслеживанию карт в рамках читателей. Эти подпрограммы обычно используют структуру [**бросить \_ реадерстате**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) в массиве.



| Раздел                                                | Описание                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**скардлокатекардс**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Поиск карточки, [*строка ATR*](../secgloss/a-gly.md) которой соответствует указанному имени карты. |
| [**скарджетстатусчанже**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Блокировать выполнение до тех пор, пока текущая доступность карт не изменится.                                                                       |
| [**скардканцел**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Завершение невыполненных действий.                                                                                                         |



 

 

 
