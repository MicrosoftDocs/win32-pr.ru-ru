---
description: Интерфейс Ивиапропертистораже предоставляет методы для чтения и записи свойств элемента для получения изображения Windows (WIA). К свойствам элементов относятся команды устройств, сведения о формате элемента и сведения об устройстве.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Чтение и задание свойств WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145379"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="5a318-104">Чтение и задание свойств WIA</span><span class="sxs-lookup"><span data-stu-id="5a318-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="5a318-105">Интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) предоставляет методы для чтения и записи свойств элемента для получения изображения Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="5a318-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="5a318-106">К свойствам элементов относятся команды устройств, сведения о формате элемента и сведения об устройстве.</span><span class="sxs-lookup"><span data-stu-id="5a318-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="5a318-107">Приложение может получить указатель на интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) элемента, перечисляя сведения об устройстве или сведения о событии путем вызова [**Ивиаитем:: енумдевицекапабилитиес**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) или [**ивиаитем:: енумрегистеревентинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) или путем запроса к интерфейсу [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) элемента.</span><span class="sxs-lookup"><span data-stu-id="5a318-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="5a318-108">(В WIA 2,0 это можно сделать путем вызова [**IWiaItem2:: енумдевицекапабилитиес**](-wia-iwiaitem2-enumdevicecapabilities.md) или [**IWiaItem2:: енумрегистеревентинфо**](-wia-iwiaitem2-enumregistereventinfo.md) или путем запроса к интерфейсу [**IWiaItem2**](-wia-iwiaitem2.md) элемента.)</span><span class="sxs-lookup"><span data-stu-id="5a318-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="5a318-109">[**Ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) наследует от [ипропертистораже](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) , а унаследованные методы реализуются, как описано в разделе Справочник по структурированному хранилищу в пакете средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="5a318-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="5a318-110">Приложения WIA должны всегда считывать заголовки данных изображений для получения точных сведений об изображении.</span><span class="sxs-lookup"><span data-stu-id="5a318-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="5a318-111">Драйвер WIA может изменять свойства WIA и заголовки данных изображения во время перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="5a318-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="5a318-112">Если отсутствует заголовок данных изображения в указанном формате, приложение WIA должно использовать свойства WIA в качестве источника информации о передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="5a318-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="5a318-113">Приложение WIA должно повторно считывать необходимые свойства WIA после завершения сканирования или записи, чтобы получить обновленные параметры.</span><span class="sxs-lookup"><span data-stu-id="5a318-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="5a318-114">В следующих разделах описываются различные свойства WIA:</span><span class="sxs-lookup"><span data-stu-id="5a318-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="5a318-115">Проверка свойства WIA</span><span class="sxs-lookup"><span data-stu-id="5a318-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="5a318-116">Свойства сведений об устройстве</span><span class="sxs-lookup"><span data-stu-id="5a318-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="5a318-117">Свойства устройства</span><span class="sxs-lookup"><span data-stu-id="5a318-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="5a318-118">Свойства элемента</span><span class="sxs-lookup"><span data-stu-id="5a318-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="5a318-119">Дополнительные свойства WIA</span><span class="sxs-lookup"><span data-stu-id="5a318-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="5a318-120">Определение пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="5a318-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="5a318-121">Использование пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="5a318-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="5a318-122">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="5a318-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 
