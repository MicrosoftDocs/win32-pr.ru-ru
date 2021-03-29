---
description: В следующем фрагменте кода показано создание простого объявления конференции. В этом фрагменте предполагается, что соединение с сервером ILS уже выполнено.
ms.assetid: d8ae90f3-37b0-4fc7-abf0-429f2bd97d66
title: Создание объявления конференции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19deed2f002da5379cb8a44a02bd6543d4b36f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815385"
---
# <a name="creating-a-conference-announcement"></a><span data-ttu-id="1918c-104">Создание объявления конференции</span><span class="sxs-lookup"><span data-stu-id="1918c-104">Creating a Conference Announcement</span></span>

<span data-ttu-id="1918c-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1918c-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1918c-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1918c-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1918c-107">В следующем фрагменте кода показано создание простого объявления конференции.</span><span class="sxs-lookup"><span data-stu-id="1918c-107">The following code fragment illustrates the creation of a simple conference announcement.</span></span> <span data-ttu-id="1918c-108">В этом фрагменте предполагается, что [соединение с сервером ILS](connecting-to-an-ils-server.md) уже выполнено.</span><span class="sxs-lookup"><span data-stu-id="1918c-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="1918c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="1918c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1918c-110">**итдиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="1918c-110">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="1918c-111">Изменение известной конференции</span><span class="sxs-lookup"><span data-stu-id="1918c-111">Modifying a Known Conference</span></span>](modifying-a-known-conference.md)
</dt> <dt>

[<span data-ttu-id="1918c-112">Получение адреса многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="1918c-112">Acquiring a Multicast Address</span></span>](acquiring-a-multicast-address.md)
</dt> </dl>

 

 



