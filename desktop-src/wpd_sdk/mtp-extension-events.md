---
description: События расширения MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: События расширения MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719726"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="26ae9-103">События расширения MTP</span><span class="sxs-lookup"><span data-stu-id="26ae9-103">MTP Extension Events</span></span>

<span data-ttu-id="26ae9-104">События уведомляют приложение о том, что изменения произошли на устройстве или с.</span><span class="sxs-lookup"><span data-stu-id="26ae9-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="26ae9-105">Например, приложение может зарегистрироваться для получения нотфикатионс об удалении устройства.</span><span class="sxs-lookup"><span data-stu-id="26ae9-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="26ae9-106">Коды расширенных событий поставщика</span><span class="sxs-lookup"><span data-stu-id="26ae9-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="26ae9-107">Когда производитель устройства поддерживает событие, расширенное поставщиком, его драйвер объединяет код события поставщика (UINT16) с старшим 16 разрядами идентификатора GUID **\_ \_ \_ \_ расширенных \_ событий поставщика событий WPD MTP** .</span><span class="sxs-lookup"><span data-stu-id="26ae9-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="26ae9-108">Например, если код, расширенный поставщиком, — 0xC001, то результирующий идентификатор GUID будет выглядеть так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="26ae9-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="26ae9-109">Параметры расширенных событий поставщика</span><span class="sxs-lookup"><span data-stu-id="26ae9-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="26ae9-110">Параметры для расширенного события поставщика передаются по **\_ \_ \_ \_ идентификатору события "параметр события WPD** " и **свойству "WPD" \_ события " \_ MTP \_ ext \_ \_**", которое представляет собой коллекцию **пропвариантс**.</span><span class="sxs-lookup"><span data-stu-id="26ae9-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="26ae9-111">Эти **пропвариантс** соответствуют параметрам события.</span><span class="sxs-lookup"><span data-stu-id="26ae9-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="26ae9-112">Если параметры отсутствуют, эта коллекция пуста.</span><span class="sxs-lookup"><span data-stu-id="26ae9-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="26ae9-113">См. также</span><span class="sxs-lookup"><span data-stu-id="26ae9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ae9-114">Поддержка расширений MTP</span><span class="sxs-lookup"><span data-stu-id="26ae9-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



