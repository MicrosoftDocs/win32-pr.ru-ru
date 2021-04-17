---
description: На следующей схеме показаны основные объекты, задействованные в элементах управления "встречный каталог" в интерфейсе TAPI 3. Показанные интерфейсы связаны со ссылками на соответствующие страницы.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Элементы управления каталогом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673290"
---
# <a name="directory-controls"></a><span data-ttu-id="8f508-104">Элементы управления каталогом</span><span class="sxs-lookup"><span data-stu-id="8f508-104">Directory Controls</span></span>

<span data-ttu-id="8f508-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8f508-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8f508-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8f508-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8f508-107">На следующей схеме показаны основные объекты, задействованные в элементах управления "встречный каталог" в интерфейсе TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="8f508-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="8f508-108">Показанные интерфейсы связаны со ссылками на соответствующие страницы.</span><span class="sxs-lookup"><span data-stu-id="8f508-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![встречные объекты и интерфейсы управления каталогом](images/renddir.png)

<span data-ttu-id="8f508-110">Основной интерфейс управления каталогом — [**итрендезваус**](/windows/desktop/api/Rend/nn-rend-itrendezvous), который должен быть создан путем вызова **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="8f508-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="8f508-111">Объект встреч предоставляет методы для получения списков доступных каталогов и для создания новых каталогов или объектов каталога.</span><span class="sxs-lookup"><span data-stu-id="8f508-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="8f508-112">Каталог находится на сервере и представляет собой список объектов каталога вместе с описательными сведениями.</span><span class="sxs-lookup"><span data-stu-id="8f508-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="8f508-113">Методы, связанные с [**итдиректори**](/windows/desktop/api/Rend/nn-rend-itdirectory) , могут получать сведения, связанные с каталогом в целом, например, является ли он каталогом ILS.</span><span class="sxs-lookup"><span data-stu-id="8f508-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="8f508-114">Объект каталога может представлять конференцию или пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f508-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="8f508-115">Интерфейс [**итдиректорйобжект**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) предоставляет методы, которые могут извлекать или изменять сведения, являющиеся общими для объекта каталога, такие как адрес для набора.</span><span class="sxs-lookup"><span data-stu-id="8f508-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="8f508-116">Сведения о Конференции и пользователя, такие как URL-адрес Конференции или основной IP-телефон пользователя, управляются методами, предоставляемыми в интерфейсах [**итдиректорйобжектконференце**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) и [**итдиректорйобжектусер**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .</span><span class="sxs-lookup"><span data-stu-id="8f508-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



