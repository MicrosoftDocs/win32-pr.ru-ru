---
description: Функции сетевого файла позволяют отслеживать и закрывать ресурсы файла, устройства и канала, открытые на сервере. Ниже перечислены функции файлов.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Функции Нетфиле (Управление сетевыми ресурсами)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674205"
---
# <a name="netfile-functions-network-share-management"></a><span data-ttu-id="2aecd-104">Функции Нетфиле (Управление сетевыми ресурсами)</span><span class="sxs-lookup"><span data-stu-id="2aecd-104">NetFile Functions (Network Share Management)</span></span>

<span data-ttu-id="2aecd-105">Функции сетевого файла позволяют отслеживать и закрывать ресурсы файла, устройства и канала, открытые на сервере.</span><span class="sxs-lookup"><span data-stu-id="2aecd-105">The network file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="2aecd-106">Ниже перечислены функции файлов.</span><span class="sxs-lookup"><span data-stu-id="2aecd-106">The file functions are listed following.</span></span>



| <span data-ttu-id="2aecd-107">Функция</span><span class="sxs-lookup"><span data-stu-id="2aecd-107">Function</span></span>                                 | <span data-ttu-id="2aecd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2aecd-108">Description</span></span>                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="2aecd-109">**нетфилеклосе**</span><span class="sxs-lookup"><span data-stu-id="2aecd-109">**NetFileClose**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="2aecd-110">Принудительное закрытие ресурса.</span><span class="sxs-lookup"><span data-stu-id="2aecd-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="2aecd-111">**нетфилинум**</span><span class="sxs-lookup"><span data-stu-id="2aecd-111">**NetFileEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="2aecd-112">Возвращает сведения об открытых файлах на сервере.</span><span class="sxs-lookup"><span data-stu-id="2aecd-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="2aecd-113">**нетфилежетинфо**</span><span class="sxs-lookup"><span data-stu-id="2aecd-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="2aecd-114">Возвращает сведения об определенном открытии ресурса сервера.</span><span class="sxs-lookup"><span data-stu-id="2aecd-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="2aecd-115">Вызовите функцию [**нетфилеклосе**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) , если файл не может быть закрыт каким бы то ни было другим способом.</span><span class="sxs-lookup"><span data-stu-id="2aecd-115">Call the [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="2aecd-116">Эту функцию следует использовать с осторожностью, так как **нетфилеклосе** не записывает данные, кэшированные в клиентской системе, в файл перед закрытием файла.</span><span class="sxs-lookup"><span data-stu-id="2aecd-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="2aecd-117">Функция [**нетфилинум**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) возвращает сведения о ресурсах, открытых на сервере.</span><span class="sxs-lookup"><span data-stu-id="2aecd-117">The [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="2aecd-118">Файл можно открыть один или несколько раз в одном или нескольких приложениях.</span><span class="sxs-lookup"><span data-stu-id="2aecd-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="2aecd-119">Каждый открывающий файл идентифицируется уникальным образом.</span><span class="sxs-lookup"><span data-stu-id="2aecd-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="2aecd-120">Функция **нетфилинум** возвращает запись для каждого открытия файла.</span><span class="sxs-lookup"><span data-stu-id="2aecd-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="2aecd-121">Функция [**нетфилежетинфо**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) возвращает сведения об одном открытии ресурса.</span><span class="sxs-lookup"><span data-stu-id="2aecd-121">The [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="2aecd-122">Сведения о файле доступны на следующих уровнях.</span><span class="sxs-lookup"><span data-stu-id="2aecd-122">File information is available at the following levels.</span></span>

<dl>

[<span data-ttu-id="2aecd-123">**\_Сведения о файле \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2aecd-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[<span data-ttu-id="2aecd-124">**\_Сведения о файле \_ 3**</span><span class="sxs-lookup"><span data-stu-id="2aecd-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

<span data-ttu-id="2aecd-125">Уровни 0 и 1 не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2aecd-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="2aecd-126">Уровень 2 возвращает только идентификационный номер, назначенный ресурсу при его открытии.</span><span class="sxs-lookup"><span data-stu-id="2aecd-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="2aecd-127">Уровень 3 Возвращает идентификационный номер, разрешения, блокировки файлов и имя пользователя, открывшего ресурс.</span><span class="sxs-lookup"><span data-stu-id="2aecd-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="2aecd-128">При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции [**нетфилинум**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) и [**нетфилежетинфо**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) .</span><span class="sxs-lookup"><span data-stu-id="2aecd-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="2aecd-129">Дополнительные сведения см. в разделе [**иадсресаурце**](/windows/desktop/api/iads/nn-iads-iadsresource) и [**иадсфилесервицеоператионс**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="2aecd-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
