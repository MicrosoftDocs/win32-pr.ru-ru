---
description: Указывает категорию PnP-X, к которой принадлежит устройство. Можно указать более одной категории.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Пнпксдевицекатегори, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693123"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="81745-104">Пнпксдевицекатегори, элемент</span><span class="sxs-lookup"><span data-stu-id="81745-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="81745-105">Указывает категорию PnP-X, к которой принадлежит устройство.</span><span class="sxs-lookup"><span data-stu-id="81745-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="81745-106">Можно указать более одной категории.</span><span class="sxs-lookup"><span data-stu-id="81745-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="81745-107">Использование</span><span class="sxs-lookup"><span data-stu-id="81745-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="81745-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="81745-108">Attributes</span></span>

<span data-ttu-id="81745-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="81745-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="81745-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="81745-110">Child elements</span></span>

<span data-ttu-id="81745-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="81745-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="81745-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="81745-112">Parent elements</span></span>



| <span data-ttu-id="81745-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="81745-113">Element</span></span>                                                   | <span data-ttu-id="81745-114">Описание</span><span class="sxs-lookup"><span data-stu-id="81745-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81745-115">**сисмоделметадата**</span><span class="sxs-lookup"><span data-stu-id="81745-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="81745-116">Определяет производителя и метаданные модели для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="81745-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="81745-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81745-117">Remarks</span></span>

<span data-ttu-id="81745-118">Устройства также могут указать подкатегорию устройства для более описательной категории устройств.</span><span class="sxs-lookup"><span data-stu-id="81745-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="81745-119">Например, "phones. WindowsMobile cameras. Дигиталстиллкамера Медиадевицес. Мусикплайер" определяет устройство, которое является устройством Microsoft Windows Mobile с камерой и музыкальным проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="81745-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="81745-120">Основной категорией устройства для этого устройства будет "phones".</span><span class="sxs-lookup"><span data-stu-id="81745-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="81745-121">Для указания нескольких категорий устройств разделяйте их пробелами.</span><span class="sxs-lookup"><span data-stu-id="81745-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="81745-122">Например, "хранилище принтеров" определяет устройство с первичной категорией "принтеры" и вторичной категорией "хранилище".</span><span class="sxs-lookup"><span data-stu-id="81745-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="81745-123">Если имеется элемент **пнпксдевицекатегори** , то по крайней мере один [**размещенный**](hosted.md) элемент должен содержать как элементы [**пнпксхардвареид**](pnpxhardwareid.md) , так и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="81745-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="81745-124">Аналогично, если элементы **пнпксхардвареид** и **пнпкскомпатиблеид** находятся в **размещенном** элементе, то внутри элемента [**сисмоделметадата**](thismodelmetadata.md) должен присутствовать хотя бы один элемент **пнпксдевицекатегори** .</span><span class="sxs-lookup"><span data-stu-id="81745-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="81745-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="81745-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="81745-126">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="81745-126">Minimum supported system</span></span><br/> | <span data-ttu-id="81745-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81745-127">Windows Vista</span></span> |
| <span data-ttu-id="81745-128">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="81745-128">Can be empty</span></span>                        | <span data-ttu-id="81745-129">Да</span><span class="sxs-lookup"><span data-stu-id="81745-129">Yes</span></span>           |



 

 




