---
description: Является корневым элементом XML-файла скрипта генератора кода WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: Всдкодежен, элемент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994681"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="e17fa-103">Всдкодежен, элемент</span><span class="sxs-lookup"><span data-stu-id="e17fa-103">wsdCodeGen element</span></span>

<span data-ttu-id="e17fa-104">Является корневым элементом XML-файла скрипта генератора кода WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="e17fa-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="e17fa-105">Использование</span><span class="sxs-lookup"><span data-stu-id="e17fa-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="e17fa-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e17fa-106">Attributes</span></span>



| <span data-ttu-id="e17fa-107">attribute</span><span class="sxs-lookup"><span data-stu-id="e17fa-107">Attribute</span></span>                        | <span data-ttu-id="e17fa-108">Тип</span><span class="sxs-lookup"><span data-stu-id="e17fa-108">Type</span></span>                             | <span data-ttu-id="e17fa-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e17fa-109">Required</span></span>       | <span data-ttu-id="e17fa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e17fa-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17fa-111">**конфигфилеверсион**</span><span class="sxs-lookup"><span data-stu-id="e17fa-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="e17fa-112">Любая символьная строка.</span><span class="sxs-lookup"><span data-stu-id="e17fa-112">Any character string.</span></span><br/> | <span data-ttu-id="e17fa-113">Да</span><span class="sxs-lookup"><span data-stu-id="e17fa-113">Yes</span></span><br/> | <span data-ttu-id="e17fa-114">Версия файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e17fa-114">The version of the configuration file.</span></span> <span data-ttu-id="e17fa-115">Единственное допустимое значение — "1,0".</span><span class="sxs-lookup"><span data-stu-id="e17fa-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="e17fa-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e17fa-116">Child elements</span></span>



| <span data-ttu-id="e17fa-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="e17fa-117">Element</span></span>                                                         | <span data-ttu-id="e17fa-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e17fa-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e17fa-119">**автостатический**</span><span class="sxs-lookup"><span data-stu-id="e17fa-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="e17fa-120">Указывает, должна ли Всдкодежен попытаться автоматически помечать определенные созданные поля как статические.</span><span class="sxs-lookup"><span data-stu-id="e17fa-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="e17fa-121">Эта функция включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e17fa-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="e17fa-122">**File**</span><span class="sxs-lookup"><span data-stu-id="e17fa-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="e17fa-123">Направляет генератору кода создать файл.</span><span class="sxs-lookup"><span data-stu-id="e17fa-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="e17fa-124">**хостметадата**</span><span class="sxs-lookup"><span data-stu-id="e17fa-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="e17fa-125">Метаданные размещения для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="e17fa-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="e17fa-126">Этот элемент используется только для реализаций устройств (узлов).</span><span class="sxs-lookup"><span data-stu-id="e17fa-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="e17fa-127">**лайернумбер**</span><span class="sxs-lookup"><span data-stu-id="e17fa-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="e17fa-128">Номер создаваемого уровня кода.</span><span class="sxs-lookup"><span data-stu-id="e17fa-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="e17fa-129">Номера слоев используются в таблицах среды выполнения для различения одного уровня кода для другого.</span><span class="sxs-lookup"><span data-stu-id="e17fa-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="e17fa-130">WSDAPI сам использует сформированный код с номером уровня 0.</span><span class="sxs-lookup"><span data-stu-id="e17fa-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="e17fa-131">**лайерпрефикс**</span><span class="sxs-lookup"><span data-stu-id="e17fa-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="e17fa-132">Префикс, используемый в созданном коде для обеспечения уникальности созданных символов.</span><span class="sxs-lookup"><span data-stu-id="e17fa-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="e17fa-133">В WSDAPI используется префикс "WSD".</span><span class="sxs-lookup"><span data-stu-id="e17fa-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="e17fa-134">**макровирусах**</span><span class="sxs-lookup"><span data-stu-id="e17fa-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="e17fa-135">Определяет текст или CDATA для повторного использования элементом [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="e17fa-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="e17fa-136">**Имен**</span><span class="sxs-lookup"><span data-stu-id="e17fa-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="e17fa-137">Описывает пространство имен, используемое для создания кода.</span><span class="sxs-lookup"><span data-stu-id="e17fa-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="e17fa-138">**релатионшипметадата**</span><span class="sxs-lookup"><span data-stu-id="e17fa-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="e17fa-139">Описывает размещение и размещение метаданных для устройства.</span><span class="sxs-lookup"><span data-stu-id="e17fa-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="e17fa-140">**сисмоделметадата**</span><span class="sxs-lookup"><span data-stu-id="e17fa-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="e17fa-141">Изготовитель и метаданные модели для реализуемого устройства.</span><span class="sxs-lookup"><span data-stu-id="e17fa-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="e17fa-142">Этот элемент используется только для реализаций устройств (узлов).</span><span class="sxs-lookup"><span data-stu-id="e17fa-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="e17fa-143">**файле**</span><span class="sxs-lookup"><span data-stu-id="e17fa-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="e17fa-144">Указывает WSDL-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="e17fa-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="e17fa-145">**схеме**</span><span class="sxs-lookup"><span data-stu-id="e17fa-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="e17fa-146">Указывает XSD-файл для обработки сведений о контракте.</span><span class="sxs-lookup"><span data-stu-id="e17fa-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="e17fa-147">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="e17fa-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="e17fa-148">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e17fa-148">Parent elements</span></span>

<span data-ttu-id="e17fa-149">Нет родительских элементов.</span><span class="sxs-lookup"><span data-stu-id="e17fa-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="e17fa-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="e17fa-150">Remarks</span></span>

<span data-ttu-id="e17fa-151">Как правило, элементы [**File**](file.md) должны выполняться последними, так как они создают код, использующий данные, указанные другими элементами.</span><span class="sxs-lookup"><span data-stu-id="e17fa-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="e17fa-152">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e17fa-152">Element information</span></span>



| <span data-ttu-id="e17fa-153">Метка</span><span class="sxs-lookup"><span data-stu-id="e17fa-153">Label</span></span> | <span data-ttu-id="e17fa-154">Значение</span><span class="sxs-lookup"><span data-stu-id="e17fa-154">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="e17fa-155">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="e17fa-155">Minimum supported system</span></span><br/> | <span data-ttu-id="e17fa-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e17fa-156">Windows Vista</span></span> |
| <span data-ttu-id="e17fa-157">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="e17fa-157">Can be empty</span></span>                        | <span data-ttu-id="e17fa-158">Да</span><span class="sxs-lookup"><span data-stu-id="e17fa-158">Yes</span></span>           |



 

 




