---
description: Свойства расширения MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Свойства расширения MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719558"
---
# <a name="mtp-extension-properties"></a><span data-ttu-id="be64a-103">Свойства расширения MTP</span><span class="sxs-lookup"><span data-stu-id="be64a-103">MTP Extension Properties</span></span>

<span data-ttu-id="be64a-104">Свойства описывают объекты, свойства, ресурсы и устройства.</span><span class="sxs-lookup"><span data-stu-id="be64a-104">Properties describe objects, properties, resources, and devices.</span></span>

## <a name="vendor-extended-object-properties"></a><span data-ttu-id="be64a-105">Поставщик — свойства расширенного объекта</span><span class="sxs-lookup"><span data-stu-id="be64a-105">Vendor-Extended Object Properties</span></span>

<span data-ttu-id="be64a-106">Когда производитель устройства создает свойство, расширенное поставщиком для объекта устройства, он объединяет свойства WPD для идентификатора GUID **\_ \_ \_ \_ расширенного \_ объекта \_ PROPS поставщика MTP** с кодом свойства объекта для создания структуры **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="be64a-106">When a device manufacturer creates a vendor-extended property for a device object, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_OBJECT\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="be64a-107">Например, если код свойства объекта — 0xD801, результирующий **PROPERTYKEY** будет выглядеть так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="be64a-107">For example, if the object's property code is 0xD801, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a><span data-ttu-id="be64a-108">Поставщик — расширенные свойства устройства</span><span class="sxs-lookup"><span data-stu-id="be64a-108">Vendor-Extended Device Properties</span></span>

<span data-ttu-id="be64a-109">Когда производитель устройства создает для устройства свойство, расширенное поставщиком, он объединяет **\_ Свойства WPD \_ \_ поставщика MTP \_ расширенных свойств \_ \_ PROPS** класса "идентификатор GUID" с кодом свойства объекта для создания структуры **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="be64a-109">When a device manufacturer creates a vendor-extended property for a device, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_DEVICE\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="be64a-110">Например, если код свойства объекта — 0xD001, результирующий **PROPERTYKEY** будет выглядеть так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="be64a-110">For example, if the object's property code is 0xD001, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a><span data-ttu-id="be64a-111">См. также</span><span class="sxs-lookup"><span data-stu-id="be64a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be64a-112">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="be64a-112">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



