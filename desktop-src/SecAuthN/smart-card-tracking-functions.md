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
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="a85d4-104">Функции отслеживания смарт-карт</span><span class="sxs-lookup"><span data-stu-id="a85d4-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="a85d4-105">Следующие функции позволяют отслеживанию карт в рамках читателей.</span><span class="sxs-lookup"><span data-stu-id="a85d4-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="a85d4-106">Эти подпрограммы обычно используют структуру [**бросить \_ реадерстате**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) в массиве.</span><span class="sxs-lookup"><span data-stu-id="a85d4-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="a85d4-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="a85d4-107">Topic</span></span>                                                | <span data-ttu-id="a85d4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a85d4-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a85d4-109">**скардлокатекардс**</span><span class="sxs-lookup"><span data-stu-id="a85d4-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="a85d4-110">Поиск карточки, [*строка ATR*](../secgloss/a-gly.md) которой соответствует указанному имени карты.</span><span class="sxs-lookup"><span data-stu-id="a85d4-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="a85d4-111">**скарджетстатусчанже**</span><span class="sxs-lookup"><span data-stu-id="a85d4-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="a85d4-112">Блокировать выполнение до тех пор, пока текущая доступность карт не изменится.</span><span class="sxs-lookup"><span data-stu-id="a85d4-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="a85d4-113">**скардканцел**</span><span class="sxs-lookup"><span data-stu-id="a85d4-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="a85d4-114">Завершение невыполненных действий.</span><span class="sxs-lookup"><span data-stu-id="a85d4-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
