---
description: Следующий фрагмент кода иллюстрирует публикацию объекта пользователя на сервере ILS. После публикации объекта пользователя удаленные стороны могут использовать объект пользователя для выполнения вызовов указанного пользователя.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Добавление объекта пользователя на сервер ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809238"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="a316a-104">Добавление объекта пользователя на сервер ILS</span><span class="sxs-lookup"><span data-stu-id="a316a-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="a316a-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a316a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a316a-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a316a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a316a-107">Следующий фрагмент кода иллюстрирует публикацию объекта пользователя на сервере ILS.</span><span class="sxs-lookup"><span data-stu-id="a316a-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="a316a-108">После публикации объекта пользователя удаленные стороны могут использовать объект пользователя для выполнения вызовов указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a316a-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="a316a-109">В этом фрагменте предполагается, что [соединение с сервером ILS](connecting-to-an-ils-server.md) уже выполнено.</span><span class="sxs-lookup"><span data-stu-id="a316a-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="a316a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a316a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a316a-111">**итдиректори**</span><span class="sxs-lookup"><span data-stu-id="a316a-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="a316a-112">**итдиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="a316a-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="a316a-113">**итдиректорйобжектусер**</span><span class="sxs-lookup"><span data-stu-id="a316a-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



