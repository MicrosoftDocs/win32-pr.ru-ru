---
description: Свойство Конфигураблеитемс только для чтения объекта Merge Возвращает коллекцию объектов Конфигураблеитем, каждый из которых представляет одну строку из таблицы Модулеконфигуратион.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configсвойство Ураблеитемс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675361"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="3a167-103">Merge.Config, свойство Ураблеитемс</span><span class="sxs-lookup"><span data-stu-id="3a167-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="3a167-104">Свойство **конфигураблеитемс** только для чтения объекта [**Merge**](merge-object.md) Возвращает коллекцию объектов [**конфигураблеитем**](configurableitem-object.md) , каждый из которых представляет одну строку из [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="3a167-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="3a167-105">В семантическом виде каждый интерфейс в перечислителе представляет элемент, который может быть настроен потребителем модуля.</span><span class="sxs-lookup"><span data-stu-id="3a167-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="3a167-106">Коллекция является коллекцией только для чтения и реализует стандартные интерфейсы коллекции только для чтения элементов (), Count () и \_ NewEnum ().</span><span class="sxs-lookup"><span data-stu-id="3a167-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="3a167-107">Перечислитель **иенуммсмконфигитемс** реализует следующие (), Skip (), Reset () и Clone () со стандартной семантикой.</span><span class="sxs-lookup"><span data-stu-id="3a167-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="3a167-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3a167-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a167-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a167-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="3a167-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a167-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="3a167-111">C++</span><span class="sxs-lookup"><span data-stu-id="3a167-111">C++</span></span>

<span data-ttu-id="3a167-112">См. раздел [**Получение функции \_ конфигураблеитемс**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) .</span><span class="sxs-lookup"><span data-stu-id="3a167-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a167-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3a167-113">Requirements</span></span>



| <span data-ttu-id="3a167-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3a167-114">Requirement</span></span> | <span data-ttu-id="3a167-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3a167-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a167-116">Версия</span><span class="sxs-lookup"><span data-stu-id="3a167-116">Version</span></span><br/> | <span data-ttu-id="3a167-117">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3a167-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3a167-118">Header</span><span class="sxs-lookup"><span data-stu-id="3a167-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3a167-119"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a167-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a167-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3a167-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a167-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a167-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




