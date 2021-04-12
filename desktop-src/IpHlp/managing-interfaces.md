---
description: Служба поддержки IP-адресов расширяет возможности управления сетевыми интерфейсами. Между интерфейсами и адаптерами на данном компьютере имеется однозначное соответствие. Интерфейс — это абстракция на уровне IP, тогда как адаптер является абстракцией на уровне канала передачи.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Управление интерфейсами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264398"
---
# <a name="managing-interfaces"></a><span data-ttu-id="27af4-105">Управление интерфейсами</span><span class="sxs-lookup"><span data-stu-id="27af4-105">Managing Interfaces</span></span>

<span data-ttu-id="27af4-106">Служба поддержки IP-адресов расширяет возможности управления сетевыми интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="27af4-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="27af4-107">Между интерфейсами и адаптерами на данном компьютере имеется однозначное соответствие.</span><span class="sxs-lookup"><span data-stu-id="27af4-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="27af4-108">Интерфейс — это абстракция на уровне IP, тогда как адаптер является абстракцией на уровне канала передачи.</span><span class="sxs-lookup"><span data-stu-id="27af4-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="27af4-109">Используйте функции, описанные в следующих абзацах, для управления интерфейсами на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="27af4-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="27af4-110">Функция [**жетнумберофинтерфацес**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) возвращает число интерфейсов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="27af4-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="27af4-111">Функция [**жетинтерфацеинфо**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) возвращает таблицу, содержащую имена и соответствующие индексы для интерфейсов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="27af4-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="27af4-112">Примеры кода, включающие **жетинтерфацеинфо** , см. [в разделе Управление интерфейсами с помощью жетинтерфацеинфо](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="27af4-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="27af4-113">Функция [**жетфриендлифиндекс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) принимает индекс интерфейса и возвращает обратно совместимый индекс интерфейса, то есть один, использующий только младшие 24 бита.</span><span class="sxs-lookup"><span data-stu-id="27af4-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="27af4-114">Этот тип индекса иногда называют "понятным" индексом интерфейса.</span><span class="sxs-lookup"><span data-stu-id="27af4-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="27af4-115">Функция [**жетифентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) возвращает структуру [**MIB \_ ифров**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , которая содержит сведения о конкретном интерфейсе на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="27af4-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="27af4-116">Эта функция требует, чтобы вызывающий объект предоставил индекс интерфейса.</span><span class="sxs-lookup"><span data-stu-id="27af4-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="27af4-117">Функция [**жетифтабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) возвращает таблицу записей [**MIB \_ ифров**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , по одной для каждого интерфейса на компьютере.</span><span class="sxs-lookup"><span data-stu-id="27af4-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="27af4-118">Используйте функцию [**сетифентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) для изменения конфигурации определенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="27af4-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 
