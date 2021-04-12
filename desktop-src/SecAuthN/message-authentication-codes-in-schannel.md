---
description: Код проверки подлинности сообщения (MAC) используется для обнаружения незаконного изменения и подделки сообщений.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Коды проверки подлинности сообщений в SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265803"
---
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="b1fdd-103">Коды проверки подлинности сообщений в SChannel</span><span class="sxs-lookup"><span data-stu-id="b1fdd-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="b1fdd-104">[*Код проверки подлинности сообщения*](../secgloss/m-gly.md) (Mac) используется для обнаружения незаконного изменения и подделки сообщений.</span><span class="sxs-lookup"><span data-stu-id="b1fdd-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="b1fdd-105">Отправитель сообщения создает компьютер MAC, шифруя односторонний [*хэш*](../secgloss/h-gly.md) тела сообщения, используя [*ключ сеанса*](../secgloss/s-gly.md) , совместно используемый отправителем и получателем.</span><span class="sxs-lookup"><span data-stu-id="b1fdd-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="b1fdd-106">MAC добавляется к сообщению, отправляемому получателю.</span><span class="sxs-lookup"><span data-stu-id="b1fdd-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="b1fdd-107">Получатель сообщения снова создает MAC, используя общий ключ сеанса и текст сообщения, и сравнивает созданный MAC с MAC, полученным от отправителя.</span><span class="sxs-lookup"><span data-stu-id="b1fdd-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="b1fdd-108">Если эти два идентичны, то отправитель должен иметь общий ключ сеанса, и сообщение не было изменено при передаче.</span><span class="sxs-lookup"><span data-stu-id="b1fdd-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="b1fdd-109">В протоколах SChannel алгоритм, используемый для создания компьютера MAC, определяется [набором шифров](cipher-suites-in-schannel.md) , который используется отправителем и получателем.</span><span class="sxs-lookup"><span data-stu-id="b1fdd-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
