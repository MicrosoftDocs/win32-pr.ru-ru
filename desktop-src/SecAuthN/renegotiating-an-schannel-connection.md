---
description: Чтобы изменить атрибуты подключения, такие как набор шифров или проверка подлинности клиента, можно запросить &\# 0034; повтор&\# 0034; или повторное согласование соединения.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Повторное согласование подключения Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650765"
---
# <a name="renegotiating-an-schannel-connection"></a><span data-ttu-id="0de6d-103">Повторное согласование подключения Schannel</span><span class="sxs-lookup"><span data-stu-id="0de6d-103">Renegotiating an Schannel Connection</span></span>

<span data-ttu-id="0de6d-104">Чтобы изменить атрибуты подключения, такие как набор шифров или проверка подлинности клиента, можно запросить повтор или повторное согласование соединения.</span><span class="sxs-lookup"><span data-stu-id="0de6d-104">To change a connection's attributes, such as the cipher suite or client authentication, you can request a "redo" or renegotiation of the connection.</span></span>

<span data-ttu-id="0de6d-105">Если изменяемые атрибуты контролируются учетными данными, необходимо получить новые учетные данные перед повторной согласованием соединения.</span><span class="sxs-lookup"><span data-stu-id="0de6d-105">If the attributes you want to change are controlled by credentials, you must obtain new credentials before you renegotiate the connection.</span></span> <span data-ttu-id="0de6d-106">Дополнительные сведения см. в разделе [Получение учетных данных SChannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="0de6d-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

<span data-ttu-id="0de6d-107">Чтобы запросить повтор из клиентского приложения, вызовите функцию [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="0de6d-107">To request a redo from a client application, call the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="0de6d-108">Серверные приложения вызывают функцию [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="0de6d-108">Server applications call the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="0de6d-109">Задайте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0de6d-109">Set the parameters as follows:</span></span>

-   <span data-ttu-id="0de6d-110">Укажите существующий [*контекст безопасности*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) в параметре *фконтекст* .</span><span class="sxs-lookup"><span data-stu-id="0de6d-110">Specify the existing [*security context*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) in the *phContext* parameter.</span></span>
-   <span data-ttu-id="0de6d-111">(Только для клиентов) Укажите то же имя сервера (в параметре *псзтаржетнаме* ), как указано при установке контекста.</span><span class="sxs-lookup"><span data-stu-id="0de6d-111">(Clients only) Specify the same server name (in the *pszTargetName* parameter) as specified when establishing the context.</span></span>
-   <span data-ttu-id="0de6d-112">Укажите новые учетные данные с помощью параметра *фкредентиал* , если это применимо.</span><span class="sxs-lookup"><span data-stu-id="0de6d-112">Specify new credentials, using the *phCredential* parameter, if applicable.</span></span>
-   <span data-ttu-id="0de6d-113">Если вы хотите изменить атрибуты контекста, не связанные с учетными данными, укажите эти атрибуты с помощью параметра *фконтекстрек* .</span><span class="sxs-lookup"><span data-stu-id="0de6d-113">If you want to change context attributes unrelated to the credentials, specify these attributes using the *fContextReq* parameter.</span></span>

<span data-ttu-id="0de6d-114">После вызова соответствующей функции приложение должно отправить результаты клиенту и продолжить обработку входящих сообщений с помощью функции [**декриптмессаже (Schannel)**](decryptmessage--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="0de6d-114">After calling the appropriate function, your application should send the results to the client and continue processing incoming messages using the [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function.</span></span>

<span data-ttu-id="0de6d-115">Функция [**декриптмессаже (Schannel)**](decryptmessage--schannel.md) возвратит ответ, \_ когда я буду повторно \_ согласовывать, когда канал Schannel готов для продолжения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="0de6d-115">The [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function will return SEC\_I\_RENEGOTIATE when Schannel is ready for your application to proceed.</span></span> <span data-ttu-id="0de6d-116">Когда вы получаете повторное \_ \_ согласование кода возврата в секунду, приложение должно вызвать [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (Servers) или [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (клиенты) и передать содержимое SECBUFFER_EXTRA, возвращенное из декриптмессаже в SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="0de6d-116">When you receive the SEC\_I\_RENEGOTIATE return code, your application must call [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servers) or [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clients), and pass the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="0de6d-117">После того как этот вызов вернет значение, продолжайте, как будто приложение создает новое соединение.</span><span class="sxs-lookup"><span data-stu-id="0de6d-117">After this call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 
