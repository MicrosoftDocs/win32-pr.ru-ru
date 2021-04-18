---
description: Подключение к определенной смарт-карте и взаимодействие с ней.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Функции смарт-карт и доступа для чтения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664168"
---
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="9574b-103">Функции смарт-карт и доступа для чтения</span><span class="sxs-lookup"><span data-stu-id="9574b-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="9574b-104">Следующие функции подключаются к определенной [*смарт-карте*](../secgloss/s-gly.md)и обмениваются данными с ней.</span><span class="sxs-lookup"><span data-stu-id="9574b-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="9574b-105">Операции ввода-вывода на карточке используют буфер для отправки или получения данных, а также структуру, содержащую сведения об управлении протоколом.</span><span class="sxs-lookup"><span data-stu-id="9574b-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="9574b-106">Структура сведений об управлении протоколом всегда начинается с [**структуры \_ \_ запроса ввода-вывода бросить**](scard-io-request.md) .</span><span class="sxs-lookup"><span data-stu-id="9574b-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="9574b-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="9574b-107">Topic</span></span>                                                  | <span data-ttu-id="9574b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9574b-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9574b-109">**скардконнект**</span><span class="sxs-lookup"><span data-stu-id="9574b-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="9574b-110">Подключитесь к карточке.</span><span class="sxs-lookup"><span data-stu-id="9574b-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="9574b-111">**скардреконнект**</span><span class="sxs-lookup"><span data-stu-id="9574b-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="9574b-112">Повторное создание соединения.</span><span class="sxs-lookup"><span data-stu-id="9574b-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="9574b-113">**скарддисконнект**</span><span class="sxs-lookup"><span data-stu-id="9574b-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="9574b-114">Завершение соединения.</span><span class="sxs-lookup"><span data-stu-id="9574b-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="9574b-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="9574b-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="9574b-116">Запуск [*транзакции*](../secgloss/t-gly.md)с блокированием доступа других приложений к карточке.</span><span class="sxs-lookup"><span data-stu-id="9574b-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="9574b-117">**скардендтрансактион**</span><span class="sxs-lookup"><span data-stu-id="9574b-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="9574b-118">Завершение транзакции, что позволяет другим приложениям получить доступ к карточке.</span><span class="sxs-lookup"><span data-stu-id="9574b-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="9574b-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="9574b-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="9574b-120">Укажите текущее состояние модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="9574b-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="9574b-121">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="9574b-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="9574b-122">Запрашивает службу и получает данные из карточки с помощью [*t = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)и необработанных протоколов.</span><span class="sxs-lookup"><span data-stu-id="9574b-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 
