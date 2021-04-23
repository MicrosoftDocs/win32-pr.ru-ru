---
title: Операции управления доступом и записи
description: Если вызывающий объект не имеет достаточных прав, изменения свойств завершаются ошибкой.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Операции контроля доступа и записи в AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890359"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="fe0f2-104">Операции управления доступом и записи</span><span class="sxs-lookup"><span data-stu-id="fe0f2-104">Access Control and Write Operations</span></span>

<span data-ttu-id="fe0f2-105">Если вызывающий объект не имеет достаточных прав, изменения свойств завершаются ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="fe0f2-106">Для операций записи, которые пакетно изменяет несколько свойств, вся операция завершается ошибкой, если вызывающий объект не имеет необходимых прав на одно из измененных свойств.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="fe0f2-107">Например, можно выполнить несколько вызовов метода [**iAds::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) , чтобы задать несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="fe0f2-108">Однако при вызове функции [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) для записи новых данных из локального кэша в каталог происходит сбой **сетинфо** , если вызывающий объект не имеет доступа на запись ко всем измененным свойствам.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="fe0f2-109">Аналогичным образом, метод [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) не может установить какие бы то ни было свойства, если у вызывающего объекта нет доступа ко всем заданным свойствам.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="fe0f2-110">Поэтому следует выполнять пакетную обработку нескольких операций изменения только в том случае, если известно, что все изменения будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="fe0f2-111">Чтобы определить атрибуты объекта каталога, которые вызывающий объект может изменять, прочтите атрибут **алловедаттрибутесеффективе** объекта.</span><span class="sxs-lookup"><span data-stu-id="fe0f2-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="fe0f2-112">Если вызывающий объект не имеет достаточных прав для изменения свойства, могут возвращаться следующие коды возврата:</span><span class="sxs-lookup"><span data-stu-id="fe0f2-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="fe0f2-113">\_свойство e \_ ADS \_ не \_ установлено \_ свойство e \_ ADS \_ не \_ изменено</span><span class="sxs-lookup"><span data-stu-id="fe0f2-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 