---
description: Интерфейс Иупдатеколлектион определяет следующие свойства.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Свойства Иупдатеколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701634"
---
# <a name="iupdatecollection-properties"></a><span data-ttu-id="91e1b-103">Свойства Иупдатеколлектион</span><span class="sxs-lookup"><span data-stu-id="91e1b-103">IUpdateCollection Properties</span></span>

<span data-ttu-id="91e1b-104">Интерфейс [**иупдатеколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="91e1b-104">The [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) interface defines the following properties.</span></span>



| <span data-ttu-id="91e1b-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="91e1b-105">Property</span></span>                                        | <span data-ttu-id="91e1b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="91e1b-106">Description</span></span>                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91e1b-107">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="91e1b-107">**\_NewEnum**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | <span data-ttu-id="91e1b-108">Возвращает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="91e1b-108">Gets an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface that can be used to enumerate the collection.</span></span> |
| [<span data-ttu-id="91e1b-109">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="91e1b-109">**Count**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | <span data-ttu-id="91e1b-110">Получает количество элементов коллекции.</span><span class="sxs-lookup"><span data-stu-id="91e1b-110">Gets the number of elements in the collection.</span></span>                                                                           |
| [<span data-ttu-id="91e1b-111">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="91e1b-111">**Item**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | <span data-ttu-id="91e1b-112">Возвращает или задает интерфейс [**иупдате**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="91e1b-112">Gets or sets an [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) interface in a collection.</span></span>                                                    |
| [<span data-ttu-id="91e1b-113">**Доступно**</span><span class="sxs-lookup"><span data-stu-id="91e1b-113">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | <span data-ttu-id="91e1b-114">Возвращает логическое значение, указывающее, доступна ли коллекция обновлений только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91e1b-114">Gets a Boolean value that indicates whether the update collection is read-only.</span></span>                                          |



 

 

 
