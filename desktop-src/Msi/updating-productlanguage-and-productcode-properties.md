---
description: Для нового языка свойство Продуктлангуаже должно быть обновлено до числового идентификатора языка (LANGID).
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Обновление свойств Продуктлангуаже и ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674303"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="86c78-103">Обновление свойств Продуктлангуаже и ProductCode</span><span class="sxs-lookup"><span data-stu-id="86c78-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="86c78-104">Для нового языка свойство [**продуктлангуаже**](productlanguage.md) должно быть обновлено до числового идентификатора языка (LangID).</span><span class="sxs-lookup"><span data-stu-id="86c78-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="86c78-105">В случае с примером локализации значение свойства **продуктлангуаже** должно быть изменено с LangID для английского (1033) на LangID для французского языка (1036) в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="86c78-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="86c78-106">Значение свойства [**ProductCode**](productcode.md) в [таблице свойств](property-table.md) должно быть изменено на новое уникальное значение при локализации базы данных, поскольку локализованный продукт считается другим продуктом.</span><span class="sxs-lookup"><span data-stu-id="86c78-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="86c78-107">Например, Немецкая и английская версии приложения считаются двумя разными продуктами и должны иметь разные коды продуктов.</span><span class="sxs-lookup"><span data-stu-id="86c78-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="86c78-108">См. [коды продуктов](product-codes.md).</span><span class="sxs-lookup"><span data-stu-id="86c78-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="86c78-109">Используйте редактор таблиц базы данных, чтобы обновить значения свойств ProductCode и Продуктлангуаже в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="86c78-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="86c78-110">Не используйте повторно идентификатор GUID, показанный при копировании этого примера.</span><span class="sxs-lookup"><span data-stu-id="86c78-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="86c78-111">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="86c78-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="86c78-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="86c78-112">Property</span></span>                                   | <span data-ttu-id="86c78-113">Значение</span><span class="sxs-lookup"><span data-stu-id="86c78-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="86c78-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="86c78-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="86c78-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="86c78-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="86c78-116">**продуктлангуаже**</span><span class="sxs-lookup"><span data-stu-id="86c78-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="86c78-117">1036</span><span class="sxs-lookup"><span data-stu-id="86c78-117">1036</span></span>                                   |



 

[<span data-ttu-id="86c78-118">Продолжить</span><span class="sxs-lookup"><span data-stu-id="86c78-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



