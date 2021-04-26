---
description: Указывает категорию PnP-X, к которой принадлежит устройство. Можно указать более одной категории.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Пнпксдевицекатегори, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996591"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="810c3-104">Пнпксдевицекатегори, элемент</span><span class="sxs-lookup"><span data-stu-id="810c3-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="810c3-105">Указывает категорию PnP-X, к которой принадлежит устройство.</span><span class="sxs-lookup"><span data-stu-id="810c3-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="810c3-106">Можно указать более одной категории.</span><span class="sxs-lookup"><span data-stu-id="810c3-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="810c3-107">Использование</span><span class="sxs-lookup"><span data-stu-id="810c3-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="810c3-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="810c3-108">Attributes</span></span>

<span data-ttu-id="810c3-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="810c3-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="810c3-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="810c3-110">Child elements</span></span>

<span data-ttu-id="810c3-111">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="810c3-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="810c3-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="810c3-112">Parent elements</span></span>



| <span data-ttu-id="810c3-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="810c3-113">Element</span></span>                                                   | <span data-ttu-id="810c3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="810c3-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="810c3-115">**сисмоделметадата**</span><span class="sxs-lookup"><span data-stu-id="810c3-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="810c3-116">Определяет производителя и метаданные модели для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="810c3-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="810c3-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="810c3-117">Remarks</span></span>

<span data-ttu-id="810c3-118">Устройства также могут указать подкатегорию устройства для более описательной категории устройств.</span><span class="sxs-lookup"><span data-stu-id="810c3-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="810c3-119">Например, "phones. WindowsMobile cameras. Дигиталстиллкамера Медиадевицес. Мусикплайер" определяет устройство, которое является устройством Microsoft Windows Mobile с камерой и музыкальным проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="810c3-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="810c3-120">Основной категорией устройства для этого устройства будет "phones".</span><span class="sxs-lookup"><span data-stu-id="810c3-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="810c3-121">Для указания нескольких категорий устройств разделяйте их пробелами.</span><span class="sxs-lookup"><span data-stu-id="810c3-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="810c3-122">Например, "хранилище принтеров" определяет устройство с первичной категорией "принтеры" и вторичной категорией "хранилище".</span><span class="sxs-lookup"><span data-stu-id="810c3-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="810c3-123">Если имеется элемент **пнпксдевицекатегори** , то по крайней мере один [**размещенный**](hosted.md) элемент должен содержать как элементы [**пнпксхардвареид**](pnpxhardwareid.md) , так и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="810c3-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="810c3-124">Аналогично, если элементы **пнпксхардвареид** и **пнпкскомпатиблеид** находятся в **размещенном** элементе, то внутри элемента [**сисмоделметадата**](thismodelmetadata.md) должен присутствовать хотя бы один элемент **пнпксдевицекатегори** .</span><span class="sxs-lookup"><span data-stu-id="810c3-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="810c3-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="810c3-125">Element information</span></span>



| <span data-ttu-id="810c3-126">Метка</span><span class="sxs-lookup"><span data-stu-id="810c3-126">Label</span></span> | <span data-ttu-id="810c3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="810c3-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="810c3-128">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="810c3-128">Minimum supported system</span></span><br/> | <span data-ttu-id="810c3-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="810c3-129">Windows Vista</span></span> |
| <span data-ttu-id="810c3-130">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="810c3-130">Can be empty</span></span>                        | <span data-ttu-id="810c3-131">Да</span><span class="sxs-lookup"><span data-stu-id="810c3-131">Yes</span></span>           |



 

 




