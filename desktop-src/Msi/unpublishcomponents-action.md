---
description: Действие Унпублишкомпонентс управляет необъявлением компонентов, перечисленных в таблице Публишкомпонент.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Действие Унпублишкомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104424306"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="0df83-103">Действие Унпублишкомпонентс</span><span class="sxs-lookup"><span data-stu-id="0df83-103">UnpublishComponents Action</span></span>

<span data-ttu-id="0df83-104">Действие Унпублишкомпонентс управляет необъявлением компонентов, перечисленных в таблице Публишкомпонент.</span><span class="sxs-lookup"><span data-stu-id="0df83-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="0df83-105">Это компоненты, которые могут быть неисправны другими продуктами.</span><span class="sxs-lookup"><span data-stu-id="0df83-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="0df83-106">Это действие удаляет сведения о опубликованных компонентах из [таблицы публишкомпонент](publishcomponent-table.md) , для которых в данный момент выбрана соответствующая функция для удаления.</span><span class="sxs-lookup"><span data-stu-id="0df83-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0df83-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="0df83-107">Sequence Restrictions</span></span>

<span data-ttu-id="0df83-108">Ограничения последовательности отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0df83-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0df83-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="0df83-109">ActionData Messages</span></span>



| <span data-ttu-id="0df83-110">Поле</span><span class="sxs-lookup"><span data-stu-id="0df83-110">Field</span></span> | <span data-ttu-id="0df83-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="0df83-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="0df83-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0df83-112">\[1\]</span></span> | <span data-ttu-id="0df83-113">Идентификатор GUID, представляющий идентификатор компонента объявленного компонента.</span><span class="sxs-lookup"><span data-stu-id="0df83-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="0df83-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="0df83-114">\[2\]</span></span> | <span data-ttu-id="0df83-115">Квалификатор идентификатора компонента.</span><span class="sxs-lookup"><span data-stu-id="0df83-115">Qualifier of the component ID.</span></span>                               |



 

