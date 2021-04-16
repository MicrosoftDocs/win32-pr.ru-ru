---
description: Протокол записи протокола TLS обеспечивает защиту данных приложения с помощью ключей, созданных во время подтверждения.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Протокол записи TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651040"
---
# <a name="tls-record-protocol"></a><span data-ttu-id="9b207-103">Протокол записи TLS</span><span class="sxs-lookup"><span data-stu-id="9b207-103">TLS Record Protocol</span></span>

<span data-ttu-id="9b207-104">Протокол [*записи протокола TLS*](../secgloss/t-gly.md) обеспечивает защиту данных приложения с помощью ключей, созданных во время [подтверждения](tls-handshake-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="9b207-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="9b207-105">Протокол записи отвечает за защиту данных приложения и проверку его [*целостности*](../secgloss/i-gly.md) и происхождения.</span><span class="sxs-lookup"><span data-stu-id="9b207-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="9b207-106">Он управляет следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="9b207-106">It manages the following:</span></span>

-   <span data-ttu-id="9b207-107">Разделение исходящих сообщений на управляемые блоки и сборка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b207-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="9b207-108">Сжатие исходящих блоков и распаковка входящих блоков (необязательно).</span><span class="sxs-lookup"><span data-stu-id="9b207-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="9b207-109">Применение [*код проверки подлинности сообщения*](../secgloss/m-gly.md) (Mac) к исходящим сообщениям и проверка входящих сообщений с помощью Mac.</span><span class="sxs-lookup"><span data-stu-id="9b207-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="9b207-110">Шифрование исходящих сообщений и расшифровка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b207-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="9b207-111">По завершении протокола записи исходящие зашифрованные данные передаются на уровень протокола TCP для транспорта.</span><span class="sxs-lookup"><span data-stu-id="9b207-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
