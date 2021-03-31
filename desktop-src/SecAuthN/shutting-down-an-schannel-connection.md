---
description: Завершение работы подключения SChannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Завершение работы подключения SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808351"
---
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="553cb-103">Завершение работы подключения SChannel</span><span class="sxs-lookup"><span data-stu-id="553cb-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="553cb-104">Если клиент или сервер завершил работу с подключением, он должен завершить работу.</span><span class="sxs-lookup"><span data-stu-id="553cb-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="553cb-105">Другая сторона, в свою очередь, должна распознать завершение работы и удалить подключение.</span><span class="sxs-lookup"><span data-stu-id="553cb-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="553cb-106">**Завершение работы подключения SChannel**</span><span class="sxs-lookup"><span data-stu-id="553cb-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="553cb-107">Вызовите функцию [**аппликонтролтокен**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , указав \_ токен управления для завершения работы SChannel.</span><span class="sxs-lookup"><span data-stu-id="553cb-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="553cb-108">После получения значения, \_ возвращаемого в секунду E \_ ОК из [**аппликонтролтокен**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), вызовите функцию [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (клиенты) или [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Servers), передав пустые буферы.</span><span class="sxs-lookup"><span data-stu-id="553cb-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="553cb-109">Продолжайте, как если бы приложение создавало новое подключение до тех пор, пока функция не вернет значение в секундах с \_ \_ \_ истечением времени или в секунду \_ \_ , чтобы указать, что подключение завершено.</span><span class="sxs-lookup"><span data-stu-id="553cb-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="553cb-110">Отправка конечных данных удаленной стороне (если таковые имеются).</span><span class="sxs-lookup"><span data-stu-id="553cb-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="553cb-111">Вызовите [**делетесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) , чтобы освободить ресурсы, удерживаемые соединением.</span><span class="sxs-lookup"><span data-stu-id="553cb-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="553cb-112">Распознавание завершения работы</span><span class="sxs-lookup"><span data-stu-id="553cb-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="553cb-113">Функция [**декриптмессаже (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) возвращает значение секунд \_ с \_ \_ истекшим сроком действия в контексте, когда отправитель сообщения отключил соединение.</span><span class="sxs-lookup"><span data-stu-id="553cb-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="553cb-114">После получения этого возвращаемого значения выполните процедуру завершения подключения SChannel ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="553cb-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
