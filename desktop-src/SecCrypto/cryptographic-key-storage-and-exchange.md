---
description: Существуют ситуации, когда ключи должны быть экспортированы из безопасной среды поставщика служб шифрования (CSP) в пространство данных приложения. Экспортированные ключи хранятся в зашифрованных структурах больших двоичных объектов.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Хранилище криптографических ключей и Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662323"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="4646a-104">Хранилище криптографических ключей и Exchange</span><span class="sxs-lookup"><span data-stu-id="4646a-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="4646a-105">Существуют ситуации, когда ключи должны быть экспортированы из безопасной среды [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) в пространство данных приложения.</span><span class="sxs-lookup"><span data-stu-id="4646a-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="4646a-106">Экспортированные ключи хранятся в зашифрованных структурах [*больших двоичных объектов*](../secgloss/k-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4646a-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="4646a-107">Существуют две ситуации, в которых необходимо экспортировать ключи:</span><span class="sxs-lookup"><span data-stu-id="4646a-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="4646a-108">Чтобы сохранить [*сеансовый ключ*](../secgloss/s-gly.md) для последующего использования приложением, например, приложение просто шифрует файл базы данных для расшифровки позже.</span><span class="sxs-lookup"><span data-stu-id="4646a-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="4646a-109">Приложение отвечает за хранение ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="4646a-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="4646a-110">Это необходимо, поскольку CSP не сохраняют [*симметричные ключи*](../secgloss/s-gly.md) из сеанса в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4646a-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="4646a-111">Чтобы отправить ключ другому лицу.</span><span class="sxs-lookup"><span data-stu-id="4646a-111">To send a key to someone else.</span></span> <span data-ttu-id="4646a-112">Это было бы проще, если соответствующие CSP могут обмениваться данными напрямую, но они не могут.</span><span class="sxs-lookup"><span data-stu-id="4646a-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="4646a-113">Поскольку CSP не могут обмениваться данными, ключ должен быть экспортирован из одного CSP, передаваться в целевое приложение, а затем импортирован в целевой CSP.</span><span class="sxs-lookup"><span data-stu-id="4646a-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="4646a-114">Этот процесс может стать более сложным, если путь связи не является доверенным.</span><span class="sxs-lookup"><span data-stu-id="4646a-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="4646a-115">В любом случае приложение должно хранить сеансовый ключ за пределами CSP в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="4646a-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="4646a-116">Дополнительные сведения см. в разделе [процедура сохранения ключа сеанса](procedure-for-storing-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="4646a-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
