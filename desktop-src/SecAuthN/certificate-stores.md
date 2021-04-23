---
description: Сертификаты клиента и сервера должны храниться в хранилище сертификатов, доступном для процесса приложения.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Хранилища сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080541"
---
# <a name="certificate-stores"></a><span data-ttu-id="55444-103">Хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="55444-103">Certificate Stores</span></span>

<span data-ttu-id="55444-104">Сертификаты [*клиента*](/windows/desktop/SecGloss/c-gly) и [*сервера*](/windows/desktop/SecGloss/s-gly) должны храниться в [*хранилище сертификатов*](/windows/desktop/SecGloss/c-gly) , доступном для процесса приложения.</span><span class="sxs-lookup"><span data-stu-id="55444-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="55444-105">Как правило, это хранилище My, также известное как личное хранилище.</span><span class="sxs-lookup"><span data-stu-id="55444-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="55444-106">Клиентские приложения, такие как Internet Explorer, обычно используют мое хранилище текущего пользователя, а на таких серверах, как службы IIS (IIS), используется система My Store локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="55444-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="55444-107">Корневое хранилище и хранилище [*центра сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) используются, когда канал Schannel или приложение создает цепочку сертификатов для отправки на удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="55444-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="55444-108">Эти хранилища используются для проверки полученной цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="55444-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="55444-109">Дополнительные сведения см. в статье [выполнение проверки подлинности с помощью канала Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="55444-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
