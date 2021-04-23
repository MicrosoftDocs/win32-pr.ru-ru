---
title: Объект Кдромколлектион
description: Объект Кдромколлектион предоставляет способ организации и доступа к коллекции компакт-дисков или DVD-дисководов.
ms.assetid: 02429ba7-a053-42bf-9ed5-c05e13c964c0
keywords:
- Проигрыватель Windows Media Object Кдромколлектион
topic_type:
- apiref
api_name:
- CdromCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d5367a6887290f06d36225f211f42048e98ba03
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068744"
---
# <a name="cdromcollection-object"></a><span data-ttu-id="8ca77-104">Объект Кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="8ca77-104">CdromCollection Object</span></span>

<span data-ttu-id="8ca77-105">Объект **кдромколлектион** предоставляет способ организации и доступа к коллекции компакт-дисков или DVD-дисководов.</span><span class="sxs-lookup"><span data-stu-id="8ca77-105">The **CdromCollection** object provides a way to organize and access a collection of CD or DVD drives.</span></span>

<span data-ttu-id="8ca77-106">Объект **кдромколлектион** поддерживает следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8ca77-106">The **CdromCollection** object supports the following property.</span></span>



| <span data-ttu-id="8ca77-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="8ca77-107">Property</span></span>                           | <span data-ttu-id="8ca77-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8ca77-108">Description</span></span>                                                        |
|------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="8ca77-109">count</span><span class="sxs-lookup"><span data-stu-id="8ca77-109">count</span></span>](cdromcollection-count.md) | <span data-ttu-id="8ca77-110">Возвращает количество доступных дисководов компакт-дисков и дисков DVD в системе.</span><span class="sxs-lookup"><span data-stu-id="8ca77-110">Retrieves the number of available CD and DVD drives on the system.</span></span> |



 

<span data-ttu-id="8ca77-111">Объект **кдромколлектион** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8ca77-111">The **CdromCollection** object supports the following methods.</span></span>



| <span data-ttu-id="8ca77-112">Метод</span><span class="sxs-lookup"><span data-stu-id="8ca77-112">Method</span></span>                                                         | <span data-ttu-id="8ca77-113">Описание</span><span class="sxs-lookup"><span data-stu-id="8ca77-113">Description</span></span>                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ca77-114">жетбидривеспеЦифиер</span><span class="sxs-lookup"><span data-stu-id="8ca77-114">getByDriveSpecifier</span></span>](cdromcollection-getbydrivespecifier.md) | <span data-ttu-id="8ca77-115">Извлекает объект [CDROM](cdrom-object.md) , связанный с определенной буквой диска.</span><span class="sxs-lookup"><span data-stu-id="8ca77-115">Retrieves the [Cdrom](cdrom-object.md) object associated with a particular drive letter.</span></span> |
| [<span data-ttu-id="8ca77-116">Item</span><span class="sxs-lookup"><span data-stu-id="8ca77-116">item</span></span>](cdromcollection-item.md)                               | <span data-ttu-id="8ca77-117">Извлекает объект [CDROM](cdrom-object.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="8ca77-117">Retrieves the [Cdrom](cdrom-object.md) object at the given index.</span></span>                        |



 

<span data-ttu-id="8ca77-118">Доступ к объекту **кдромколлектион** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="8ca77-118">The **CdromCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="8ca77-119">Объект</span><span class="sxs-lookup"><span data-stu-id="8ca77-119">Object</span></span>                      | <span data-ttu-id="8ca77-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="8ca77-120">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="8ca77-121">Игрок</span><span class="sxs-lookup"><span data-stu-id="8ca77-121">Player</span></span>](player-object.md) | [<span data-ttu-id="8ca77-122">кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="8ca77-122">cdromCollection</span></span>](player-cdromcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="8ca77-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ca77-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca77-124">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="8ca77-124">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




