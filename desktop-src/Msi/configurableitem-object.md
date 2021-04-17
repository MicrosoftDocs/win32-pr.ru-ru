---
description: Объект Конфигураблеитем представляет одну строку из таблицы Модулеконфигуратион.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Объект Конфигураблеитем (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652196"
---
# <a name="configurableitem-object"></a><span data-ttu-id="6ca33-103">Объект Конфигураблеитем</span><span class="sxs-lookup"><span data-stu-id="6ca33-103">ConfigurableItem object</span></span>

<span data-ttu-id="6ca33-104">**Объект конфигураблеитем** представляет одну строку из [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ca33-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="6ca33-105">Это один настраиваемый атрибут "Attribute" из модуля.</span><span class="sxs-lookup"><span data-stu-id="6ca33-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="6ca33-106">Интерфейс содержит свойства только для чтения, по одному для каждого столбца в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="6ca33-107">Определение интерфейса выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6ca33-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="6ca33-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="6ca33-108">Members</span></span>

<span data-ttu-id="6ca33-109">Объект **конфигураблеитем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ca33-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="6ca33-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ca33-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ca33-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ca33-111">Properties</span></span>

<span data-ttu-id="6ca33-112">Объект **конфигураблеитем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6ca33-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="6ca33-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="6ca33-113">Property</span></span>                                                         | <span data-ttu-id="6ca33-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6ca33-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ca33-115">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="6ca33-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="6ca33-116">Возвращает значение в поле Attributes записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="6ca33-117">**Локального**</span><span class="sxs-lookup"><span data-stu-id="6ca33-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="6ca33-118">Возвращает значение в поле контекста записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="6ca33-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="6ca33-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="6ca33-120">Возвращает значение в поле DefaultValue записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="6ca33-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ca33-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="6ca33-122">Возвращает значение в поле Description записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="6ca33-123">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6ca33-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="6ca33-124">Возвращает значение в поле DisplayName записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="6ca33-125">**Формат**</span><span class="sxs-lookup"><span data-stu-id="6ca33-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="6ca33-126">Возвращает значение в поле Format записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="6ca33-127">**Данным**</span><span class="sxs-lookup"><span data-stu-id="6ca33-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="6ca33-128">Возвращает значение в поле HelpKeyword записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="6ca33-129">**HelpLocation**</span><span class="sxs-lookup"><span data-stu-id="6ca33-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="6ca33-130">Возвращает значение в поле HelpLocation записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="6ca33-131">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6ca33-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="6ca33-132">Возвращает значение в поле Name записи этого объекта в [таблице модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ca33-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="6ca33-133">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ca33-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="6ca33-134">Возвращает значение в поле Type записи этого объекта в таблице Модулеконфигуратион.</span><span class="sxs-lookup"><span data-stu-id="6ca33-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="6ca33-135">C++</span><span class="sxs-lookup"><span data-stu-id="6ca33-135">C++</span></span>

<span data-ttu-id="6ca33-136">интерфейс **имсмконфигураблеитем: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="6ca33-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="6ca33-137">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="6ca33-137">Interface ID</span></span>



| <span data-ttu-id="6ca33-138">Константа</span><span class="sxs-lookup"><span data-stu-id="6ca33-138">Constant</span></span>                      | <span data-ttu-id="6ca33-139">Значение</span><span class="sxs-lookup"><span data-stu-id="6ca33-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="6ca33-140">**IID \_ имсмконфигураблеитем**</span><span class="sxs-lookup"><span data-stu-id="6ca33-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="6ca33-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span><span class="sxs-lookup"><span data-stu-id="6ca33-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6ca33-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6ca33-142">Requirements</span></span>



| <span data-ttu-id="6ca33-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6ca33-143">Requirement</span></span> | <span data-ttu-id="6ca33-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6ca33-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca33-145">Версия</span><span class="sxs-lookup"><span data-stu-id="6ca33-145">Version</span></span><br/> | <span data-ttu-id="6ca33-146">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6ca33-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6ca33-147">Header</span><span class="sxs-lookup"><span data-stu-id="6ca33-147">Header</span></span><br/>  | <dl> <span data-ttu-id="6ca33-148"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca33-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ca33-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6ca33-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ca33-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ca33-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




