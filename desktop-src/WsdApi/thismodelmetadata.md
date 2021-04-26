---
description: Определяет производителя и метаданные модели для реализуемого устройства. Этот элемент используется только для реализаций устройств (узлов).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: Сисмоделметадата, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995341"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="ea16d-104">Сисмоделметадата, элемент</span><span class="sxs-lookup"><span data-stu-id="ea16d-104">thisModelMetadata element</span></span>

<span data-ttu-id="ea16d-105">Определяет производителя и метаданные модели для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="ea16d-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="ea16d-106">Этот элемент используется только для реализаций устройств (узлов).</span><span class="sxs-lookup"><span data-stu-id="ea16d-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="ea16d-107">Использование</span><span class="sxs-lookup"><span data-stu-id="ea16d-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="ea16d-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ea16d-108">Attributes</span></span>

<span data-ttu-id="ea16d-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ea16d-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ea16d-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ea16d-110">Child elements</span></span>



| <span data-ttu-id="ea16d-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="ea16d-111">Element</span></span>                                                     | <span data-ttu-id="ea16d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ea16d-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea16d-113">**производителя**</span><span class="sxs-lookup"><span data-stu-id="ea16d-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="ea16d-114">Имя производителя.</span><span class="sxs-lookup"><span data-stu-id="ea16d-114">Name of the manufacturer.</span></span> <span data-ttu-id="ea16d-115">В метаданных должен присутствовать по крайней мере один из [**производителей**](manufacturer.md) или [**мануфактурерлс**](manufacturerls.md) .</span><span class="sxs-lookup"><span data-stu-id="ea16d-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="ea16d-116">**мануфактурерлс**</span><span class="sxs-lookup"><span data-stu-id="ea16d-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="ea16d-117">Локализованная версия имени производителя.</span><span class="sxs-lookup"><span data-stu-id="ea16d-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="ea16d-118">**мануфактурерурл**</span><span class="sxs-lookup"><span data-stu-id="ea16d-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="ea16d-119">URL-адрес изготовителя.</span><span class="sxs-lookup"><span data-stu-id="ea16d-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="ea16d-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="ea16d-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="ea16d-121">Имя устройства.</span><span class="sxs-lookup"><span data-stu-id="ea16d-121">Name of the device.</span></span> <span data-ttu-id="ea16d-122">В метаданных должен присутствовать хотя бы один из [**modelName**](modelname.md) или [**моделнамелс**](modelnamels.md) .</span><span class="sxs-lookup"><span data-stu-id="ea16d-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="ea16d-123">**моделнамелс**</span><span class="sxs-lookup"><span data-stu-id="ea16d-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="ea16d-124">Локализованная версия имени устройства.</span><span class="sxs-lookup"><span data-stu-id="ea16d-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="ea16d-125">**моделнумбер**</span><span class="sxs-lookup"><span data-stu-id="ea16d-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="ea16d-126">Номер модели устройства.</span><span class="sxs-lookup"><span data-stu-id="ea16d-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="ea16d-127">**моделурл**</span><span class="sxs-lookup"><span data-stu-id="ea16d-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="ea16d-128">URL-адрес модели устройства.</span><span class="sxs-lookup"><span data-stu-id="ea16d-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="ea16d-129">**пнпксдевицекатегори**</span><span class="sxs-lookup"><span data-stu-id="ea16d-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="ea16d-130">Категория PnP-X, к которой принадлежит устройство.</span><span class="sxs-lookup"><span data-stu-id="ea16d-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="ea16d-131">**пресентатионурл**</span><span class="sxs-lookup"><span data-stu-id="ea16d-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="ea16d-132">URL-адрес данных представления модели устройства.</span><span class="sxs-lookup"><span data-stu-id="ea16d-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="ea16d-133">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="ea16d-133">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="ea16d-134">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ea16d-134">Parent elements</span></span>



| <span data-ttu-id="ea16d-135">Элемент</span><span class="sxs-lookup"><span data-stu-id="ea16d-135">Element</span></span>                                     | <span data-ttu-id="ea16d-136">Описание</span><span class="sxs-lookup"><span data-stu-id="ea16d-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea16d-137">**всдкодежен**</span><span class="sxs-lookup"><span data-stu-id="ea16d-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="ea16d-138">Корневой элемент XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ea16d-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ea16d-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea16d-139">Remarks</span></span>

<span data-ttu-id="ea16d-140">Метаданные производителя соответствуют разделу метаданных производителя, описанному в профиле устройства (Дополнительные сведения см. в профиле устройства).</span><span class="sxs-lookup"><span data-stu-id="ea16d-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="ea16d-141">Необходимо указать имя производителя или хотя бы одну локализованную версию имени производителя.</span><span class="sxs-lookup"><span data-stu-id="ea16d-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="ea16d-142">Необходимо указать имя модели или хотя бы одну локализованную версию имени модели.</span><span class="sxs-lookup"><span data-stu-id="ea16d-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="ea16d-143">Элемент [**сисмоделметадатадефинитион**](thismodelmetadatadefinition.md) затем используется для создания константы C, содержащей эти сведения.</span><span class="sxs-lookup"><span data-stu-id="ea16d-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="ea16d-144">Если имеется элемент [**пнпксдевицекатегори**](pnpxdevicecategory.md) , то по крайней мере один [**размещенный**](hosted.md) элемент должен содержать как элементы [**пнпксхардвареид**](pnpxhardwareid.md) , так и [**пнпкскомпатиблеид**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="ea16d-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="ea16d-145">Аналогично, если элементы **пнпксхардвареид** и **пнпкскомпатиблеид** представлены в **размещенном** элементе, элемент **пнпксдевицекатегори** должен присутствовать в элементе **сисмоделметадата** .</span><span class="sxs-lookup"><span data-stu-id="ea16d-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="ea16d-146">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ea16d-146">Element information</span></span>



| <span data-ttu-id="ea16d-147">Метка</span><span class="sxs-lookup"><span data-stu-id="ea16d-147">Label</span></span> | <span data-ttu-id="ea16d-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ea16d-148">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ea16d-149">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="ea16d-149">Minimum supported system</span></span><br/> | <span data-ttu-id="ea16d-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea16d-150">Windows Vista</span></span> |
| <span data-ttu-id="ea16d-151">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="ea16d-151">Can be empty</span></span>                        | <span data-ttu-id="ea16d-152">нет</span><span class="sxs-lookup"><span data-stu-id="ea16d-152">No</span></span>            |



 

 




