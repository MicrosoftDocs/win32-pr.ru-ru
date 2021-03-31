---
description: Семантика для датаграммы, или без соединения, немного отличаются от контекстов, ориентированных на соединение.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Контексты датаграмм
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154774"
---
# <a name="datagram-contexts"></a><span data-ttu-id="a02aa-103">Контексты датаграмм</span><span class="sxs-lookup"><span data-stu-id="a02aa-103">Datagram Contexts</span></span>

<span data-ttu-id="a02aa-104">Семантика для [*датаграммы*](/windows/desktop/SecGloss/d-gly), или без соединения, немного отличаются от контекстов, ориентированных на соединение.</span><span class="sxs-lookup"><span data-stu-id="a02aa-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="a02aa-105">В [*контексте*](/windows/desktop/SecGloss/c-gly)датаграммы без подключения сервер не может определить, когда клиент завершил работу или завершил соединение иным образом.</span><span class="sxs-lookup"><span data-stu-id="a02aa-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="a02aa-106">Иными словами, уведомление о завершении не передается из транспортного приложения на сервер, как это происходит в контексте, ориентированном на соединение.</span><span class="sxs-lookup"><span data-stu-id="a02aa-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="a02aa-107">Чтобы использовать контекст датаграммы, клиент устанавливает флаг "ISC \_ req \_ Datagram" в вызове функции [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="a02aa-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a02aa-108">Пакет [Microsoft Kerberos](microsoft-kerberos.md) не поддерживает контексты датаграмм в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="a02aa-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="a02aa-109">Для лучшей поддержки некоторых моделей, в частности RPC в стиле DCE, применяются следующие правила, если клиент использует контекст датаграммы:</span><span class="sxs-lookup"><span data-stu-id="a02aa-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="a02aa-110">[*Пакет безопасности*](/windows/desktop/SecGloss/s-gly) не создает [*BLOB*](/windows/desktop/SecGloss/b-gly) -объект проверки подлинности (большой двоичный объект) при первом вызове [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="a02aa-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="a02aa-111">Однако клиент может использовать возвращенный контекст безопасности в вызове функции [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) , чтобы создать сигнатуру для сообщения.</span><span class="sxs-lookup"><span data-stu-id="a02aa-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="a02aa-112">Пакет безопасности должен допускать многократное повторное установление контекста, чтобы разрешить серверу удалять подключение без уведомления.</span><span class="sxs-lookup"><span data-stu-id="a02aa-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="a02aa-113">Это означает, что все ключи, используемые в функциях [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , могут быть сброшены в целостное [*состояние*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="a02aa-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="a02aa-114">Пакет безопасности позволяет вызывающему объекту указать сведения о последовательности и предоставляет эту информацию о последовательности на стороне получателя.</span><span class="sxs-lookup"><span data-stu-id="a02aa-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="a02aa-115">Это дополнение к любой информации о последовательности, поддерживаемой пакетом.</span><span class="sxs-lookup"><span data-stu-id="a02aa-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="a02aa-116">Пакет безопасности устанавливает \_ флаг SECPKG флага \_ датаграммы, чтобы указать, что он поддерживает семантику датаграммы.</span><span class="sxs-lookup"><span data-stu-id="a02aa-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
