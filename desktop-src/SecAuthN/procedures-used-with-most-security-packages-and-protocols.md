---
description: Модель интерфейса поставщика поддержки безопасности (SSPI) предоставляет единый интерфейс для приложения транспорта клиента/сервера с помощью различных пакетов безопасности, доступных на компьютере или в сети.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Процедуры, используемые в большинстве пакетов и протоколов безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541162"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a><span data-ttu-id="f1728-103">Процедуры, используемые в большинстве пакетов и протоколов безопасности</span><span class="sxs-lookup"><span data-stu-id="f1728-103">Procedures Used with Most Security Packages and Protocols</span></span>

<span data-ttu-id="f1728-104">Модель [*интерфейса поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI) предоставляет единый интерфейс для приложения транспорта клиента/сервера с помощью различных [*пакетов безопасности*](../secgloss/s-gly.md) , доступных на компьютере или в сети.</span><span class="sxs-lookup"><span data-stu-id="f1728-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) model provides a single interface for a client/server transport application using the various [*security packages*](../secgloss/s-gly.md) available on a computer or network.</span></span> <span data-ttu-id="f1728-105">SSPI позволяет приложению использовать пакет безопасности без использования базовых [*протоколов безопасности*](../secgloss/s-gly.md) пакета.</span><span class="sxs-lookup"><span data-stu-id="f1728-105">SSPI allows an application to use a security package without dealing with the underlying [*security protocols*](../secgloss/s-gly.md) of the package.</span></span> <span data-ttu-id="f1728-106">В то же время SSPI также позволяет сложным приложениям, поддерживающим безопасность, использовать преимущества расширенных возможностей конкретных пакетов безопасности.</span><span class="sxs-lookup"><span data-stu-id="f1728-106">At the same time, SSPI also allows sophisticated, security-aware applications to take advantage of the advanced capabilities of specific security packages.</span></span>

<span data-ttu-id="f1728-107">Приложения инициализируют SSPI, выполнив следующие действия для обеспечения безопасности сетевого подключения для большинства пакетов безопасности:</span><span class="sxs-lookup"><span data-stu-id="f1728-107">Applications initialize SSPI using the following steps to secure a network connection for most security packages:</span></span>

-   [<span data-ttu-id="f1728-108">Использование Секбуффердеск и Pvbuffer</span><span class="sxs-lookup"><span data-stu-id="f1728-108">Using SecBufferDesc and SecBuffer</span></span>](using-secbufferdesc-and-secbuffer.md)
-   [<span data-ttu-id="f1728-109">Инициализация SSPI</span><span class="sxs-lookup"><span data-stu-id="f1728-109">Initializing SSPI</span></span>](initializing-sspi.md)
-   [<span data-ttu-id="f1728-110">Установление безопасного подключения с проверкой подлинности</span><span class="sxs-lookup"><span data-stu-id="f1728-110">Establishing a Secure Connection with Authentication</span></span>](establishing-a-secure-connection-with-authentication.md)
-   [<span data-ttu-id="f1728-111">Обеспечение целостности связи во время обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="f1728-111">Ensuring Communication Integrity During Message Exchange</span></span>](ensuring-communication-integrity-during-message-exchange.md)
-   [<span data-ttu-id="f1728-112">Завершение сеанса SSPI</span><span class="sxs-lookup"><span data-stu-id="f1728-112">Ending an SSPI Session</span></span>](ending-an-sspi-session.md)

 

 
