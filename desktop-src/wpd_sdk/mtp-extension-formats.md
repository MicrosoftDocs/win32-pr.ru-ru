---
description: Форматы расширений MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Форматы расширений MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719559"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="4763e-103">Форматы расширений MTP</span><span class="sxs-lookup"><span data-stu-id="4763e-103">MTP Extension Formats</span></span>

<span data-ttu-id="4763e-104">Формат файла на устройстве можно описать с помощью значения GUID.</span><span class="sxs-lookup"><span data-stu-id="4763e-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="4763e-105">Это значение задается \_ свойством "формат объекта WPD" \_ .</span><span class="sxs-lookup"><span data-stu-id="4763e-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="4763e-106">Поставщик — Расширенные форматы</span><span class="sxs-lookup"><span data-stu-id="4763e-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="4763e-107">Если производитель устройства поддерживает расширенный формат поставщика, его драйвер объединяет код формата поставщика (UINT16) с старшими 16 битами **\_ формата объекта WPD без \_ \_ указания** идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="4763e-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="4763e-108">Например, если код, расширенный поставщиком, — 0xB001, то результирующий идентификатор GUID будет выглядеть так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="4763e-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="4763e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4763e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4763e-110">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="4763e-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



