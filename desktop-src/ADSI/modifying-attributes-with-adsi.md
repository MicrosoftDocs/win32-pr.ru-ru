---
title: Изменение атрибутов с помощью ADSI
description: Чтобы изменить значения атрибутов, ADSI предоставляет методы IADs. Where и IADs. Путекс. Эти методы изменяют данные в кэше на стороне клиента. Для фиксации изменений в каталоге необходимо вызвать метод IADs. Сетинфо.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Изменение атрибутов с помощью ADSI
- Атрибуты ADSI, изменение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413728"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="9c8a8-107">Изменение атрибутов с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="9c8a8-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="9c8a8-108">Чтобы изменить значения атрибутов, ADSI предоставляет методы [**iAds.**](/windows/desktop/api/Iads/nf-iads-iads-put) WHERE и [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="9c8a8-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="9c8a8-109">Эти методы изменяют данные в кэше на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="9c8a8-110">Для фиксации изменений в каталоге необходимо вызвать метод [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="9c8a8-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="9c8a8-111">Если изменение нескольких атрибутов фиксируется в одном вызове [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), если какой-либо отдельный атрибут не может быть изменен, ни один из атрибутов не будет изменен.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="9c8a8-112">Например, если изменить атрибуты [**SN**](/windows/desktop/ADSchema/a-sn) и [**givenName**](/windows/desktop/ADSchema/a-givenname) и очистить атрибут [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) объекта пользователя без последующих вызовов метода **сетинфо** , изменения будут введены при вызове **сетинфо**.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="9c8a8-113">Если одно или несколько изменений не разрешены и, следовательно, не могут быть выполнены, то никакие коллективные изменения, внесенные в атрибуты, не будут введены во время вызова **сетинфо**.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="9c8a8-114">Метод [**iAds. помещаем**](/windows/desktop/api/Iads/nf-iads-iads-put) принимает имя атрибута и параметр Variant.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="9c8a8-115">Используйте этот метод, чтобы задать атрибуты, которые содержат как одно, так и несколько значений.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="9c8a8-116">Метод [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) предоставляет контроль над операциями с многозначными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="9c8a8-117">Можно добавлять, удалять, обновлять и очищать существующие значения.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="9c8a8-118">Метод **iAds. путекс** всегда принимает массив вариантов значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="9c8a8-119">Однако этот метод можно использовать для задания одного и того же значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="9c8a8-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="9c8a8-120">Метод [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) использует операции, указанные в перечислении [**\_ \_ \_ enum операции свойства ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="9c8a8-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 