---
description: Определяет производителя и метаданные модели для реализуемого устройства. Этот элемент используется только для реализаций устройств (узлов).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: Сисмоделметадата, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912219"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="0608f-104">Сисмоделметадата, элемент</span><span class="sxs-lookup"><span data-stu-id="0608f-104">thisModelMetadata element</span></span>

<span data-ttu-id="0608f-105">Определяет производителя и метаданные модели для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="0608f-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="0608f-106">Этот элемент используется только для реализаций устройств (узлов).</span><span class="sxs-lookup"><span data-stu-id="0608f-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="0608f-107">Использование</span><span class="sxs-lookup"><span data-stu-id="0608f-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="0608f-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0608f-108">Attributes</span></span>

<span data-ttu-id="0608f-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0608f-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0608f-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0608f-110">Child elements</span></span>



| <span data-ttu-id="0608f-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="0608f-111">Element</span></span>                                                     | <span data-ttu-id="0608f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0608f-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0608f-113">**производителя**</span><span class="sxs-lookup"><span data-stu-id="0608f-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="0608f-114">Имя производителя.</span><span class="sxs-lookup"><span data-stu-id="0608f-114">Name of the manufacturer.</span></span> <span data-ttu-id="0608f-115">В метаданных должен присутствовать по крайней мере один из [**производителей**](manufacturer.md) или [**мануфактурерлс**](manufacturerls.md) .</span><span class="sxs-lookup"><span data-stu-id="0608f-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="0608f-116">**мануфактурерлс**</span><span class="sxs-lookup"><span data-stu-id="0608f-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="0608f-117">Локализованная версия имени производителя.</span><span class="sxs-lookup"><span data-stu-id="0608f-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="0608f-118">**мануфактурерурл**</span><span class="sxs-lookup"><span data-stu-id="0608f-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="0608f-119">URL-адрес изготовителя.</span><span class="sxs-lookup"><span data-stu-id="0608f-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="0608f-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="0608f-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="0608f-121">Имя устройства.</span><span class="sxs-lookup"><span data-stu-id="0608f-121">Name of the device.</span></span> <span data-ttu-id="0608f-122">В метаданных должен присутствовать хотя бы один из [**modelName**](modelname.md) или [**моделнамелс**](modelnamels.md) .</span><span class="sxs-lookup"><span data-stu-id="0608f-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="0608f-123">**моделнамелс**</span><span class="sxs-lookup"><span data-stu-id="0608f-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="0608f-124">Локализованная версия имени устройства.</span><span class="sxs-lookup"><span data-stu-id="0608f-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="0608f-125">**моделнумбер**</span><span class="sxs-lookup"><span data-stu-id="0608f-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="0608f-126">Номер модели устройства.</span><span class="sxs-lookup"><span data-stu-id="0608f-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="0608f-127">**моделурл**</span><span class="sxs-lookup"><span data-stu-id="0608f-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="0608f-128">URL-адрес модели устройства.</span><span class="sxs-lookup"><span data-stu-id="0608f-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="0608f-129">**пнпксдевицекатегори**</span><span class="sxs-lookup"><span data-stu-id="0608f-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="0608f-130">Категория PnP-X, к которой принадлежит устройство.</span><span class="sxs-lookup"><span data-stu-id="0608f-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="0608f-131">**пресентатионурл**</span><span class="sxs-lookup"><span data-stu-id="0608f-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="0608f-132">URL-адрес данных представления модели устройства.</span><span class="sxs-lookup"><span data-stu-id="0608f-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="0608f-133">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="0608f-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="0608f-134">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0608f-134">Parent elements</span></span>



| <span data-ttu-id="0608f-135">Элемент</span><span class="sxs-lookup"><span data-stu-id="0608f-135">Element</span></span>                                     | <span data-ttu-id="0608f-136">Описание</span><span class="sxs-lookup"><span data-stu-id="0608f-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0608f-137">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="0608f-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0608f-138">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0608f-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0608f-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0608f-139">Remarks</span></span>

<span data-ttu-id="0608f-140">Метаданные производителя соответствуют разделу метаданных производителя, описанному в профиле устройства (Дополнительные сведения см. в профиле устройства).</span><span class="sxs-lookup"><span data-stu-id="0608f-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="0608f-141">Необходимо указать имя производителя или хотя бы одну локализованную версию имени производителя.</span><span class="sxs-lookup"><span data-stu-id="0608f-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="0608f-142">Необходимо указать имя модели или хотя бы одну локализованную версию имени модели.</span><span class="sxs-lookup"><span data-stu-id="0608f-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="0608f-143">Элемент [**сисмоделметадатадефинитион**](thismodelmetadatadefinition.md) затем используется для создания константы C, содержащей эти сведения.</span><span class="sxs-lookup"><span data-stu-id="0608f-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="0608f-144">Если имеется элемент [**пнпксдевицекатегори**](pnpxdevicecategory.md) , то по крайней мере один [**размещенный**](hosted.md) элемент должен содержать как элементы [**пнпксхардвареид**](pnpxhardwareid.md) , так и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="0608f-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="0608f-145">Аналогично, если элементы **пнпксхардвареид** и **пнпкскомпатиблеид** представлены в **размещенном** элементе, элемент **пнпксдевицекатегори** должен присутствовать в элементе **сисмоделметадата** .</span><span class="sxs-lookup"><span data-stu-id="0608f-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="0608f-146">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0608f-146">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0608f-147">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="0608f-147">Minimum supported system</span></span><br/> | <span data-ttu-id="0608f-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0608f-148">Windows Vista</span></span> |
| <span data-ttu-id="0608f-149">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="0608f-149">Can be empty</span></span>                        | <span data-ttu-id="0608f-150">Нет</span><span class="sxs-lookup"><span data-stu-id="0608f-150">No</span></span>            |



 

 




