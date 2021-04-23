---
description: Свойство Format объекта Конфигураблеитем возвращает значение из столбца Format таблицы Модулеконфигуратион.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Свойство Конфигураблеитем. Format (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651897"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="0350b-103">Конфигураблеитем. Format, свойство</span><span class="sxs-lookup"><span data-stu-id="0350b-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="0350b-104">Свойство **Format** объекта [**конфигураблеитем**](configurableitem-object.md) возвращает значение из столбца Format [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="0350b-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="0350b-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0350b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0350b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0350b-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="0350b-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0350b-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0350b-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0350b-108">Remarks</span></span>

<span data-ttu-id="0350b-109">Это свойство может иметь только следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0350b-109">This property can only have the following values.</span></span>



| <span data-ttu-id="0350b-110">Константа</span><span class="sxs-lookup"><span data-stu-id="0350b-110">Constant</span></span>                        | <span data-ttu-id="0350b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0350b-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="0350b-112">**мсмконфигураблеитемтекст**</span><span class="sxs-lookup"><span data-stu-id="0350b-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="0350b-113">0</span><span class="sxs-lookup"><span data-stu-id="0350b-113">0</span></span>     |
| <span data-ttu-id="0350b-114">**мсмконфигураблеитемкэй**</span><span class="sxs-lookup"><span data-stu-id="0350b-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="0350b-115">1</span><span class="sxs-lookup"><span data-stu-id="0350b-115">1</span></span>     |
| <span data-ttu-id="0350b-116">**мсмконфигураблеитеминтежер**</span><span class="sxs-lookup"><span data-stu-id="0350b-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="0350b-117">2</span><span class="sxs-lookup"><span data-stu-id="0350b-117">2</span></span>     |
| <span data-ttu-id="0350b-118">**мсмконфигураблеитембитфиелд**</span><span class="sxs-lookup"><span data-stu-id="0350b-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="0350b-119">3</span><span class="sxs-lookup"><span data-stu-id="0350b-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="0350b-120">C++</span><span class="sxs-lookup"><span data-stu-id="0350b-120">C++</span></span>

<span data-ttu-id="0350b-121">См. раздел [**Получение функции \_ форматирования**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) .</span><span class="sxs-lookup"><span data-stu-id="0350b-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0350b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0350b-122">Requirements</span></span>



| <span data-ttu-id="0350b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0350b-123">Requirement</span></span> | <span data-ttu-id="0350b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0350b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0350b-125">Версия</span><span class="sxs-lookup"><span data-stu-id="0350b-125">Version</span></span><br/> | <span data-ttu-id="0350b-126">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0350b-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="0350b-127">Header</span><span class="sxs-lookup"><span data-stu-id="0350b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0350b-128"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="0350b-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="0350b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0350b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="0350b-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0350b-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




