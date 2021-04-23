---
description: Запросите базу данных смарт-карты. Они могут предоставить список смарт-карт, предоставляемых определенным пользователем, интерфейсов и поставщиков основной службы определенной карты, групп читателей, определенных для системы, и читателей в наборе групп читателей.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Функции запросов к базе данных смарт-карты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265937"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="85f72-104">Функции запросов к базе данных смарт-карты</span><span class="sxs-lookup"><span data-stu-id="85f72-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="85f72-105">Следующие функции запрашивают [*базу данных смарт-карты*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85f72-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="85f72-106">Они могут предоставить список смарт-карт, предоставляемых определенным пользователем, интерфейсов и [*поставщиков основной службы*](../secgloss/p-gly.md) определенной карты, [*групп читателей*](../secgloss/r-gly.md) , определенных для системы, и [*читателей*](../secgloss/r-gly.md) в наборе групп читателей.</span><span class="sxs-lookup"><span data-stu-id="85f72-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="85f72-107">При использовании этих функций можно выполнить запрос к полной базе данных смарт-карты или уменьшить область поиска, задав [*контекст Resource Manager*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85f72-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="85f72-108">Контекст Resource Manager задается путем вызова [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) перед вызовом функции запроса.</span><span class="sxs-lookup"><span data-stu-id="85f72-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="85f72-109">Без указанного контекста некоторые сведения могут оставаться недоступными из-за ограничений безопасности.</span><span class="sxs-lookup"><span data-stu-id="85f72-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="85f72-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="85f72-110">Topic</span></span>                                                  | <span data-ttu-id="85f72-111">Описание</span><span class="sxs-lookup"><span data-stu-id="85f72-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85f72-112">**скарджетпровидерид**</span><span class="sxs-lookup"><span data-stu-id="85f72-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="85f72-113">Получение идентификатора (GUID) [*основного поставщика услуг*](../secgloss/p-gly.md) для данной карточки.</span><span class="sxs-lookup"><span data-stu-id="85f72-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="85f72-114">**скардлисткардс**</span><span class="sxs-lookup"><span data-stu-id="85f72-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="85f72-115">Получение списка карточек, ранее введенных в систему конкретным пользователем.</span><span class="sxs-lookup"><span data-stu-id="85f72-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="85f72-116">**скардлистинтерфацес**</span><span class="sxs-lookup"><span data-stu-id="85f72-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="85f72-117">Получение идентификаторов (GUID) интерфейсов, предоставленных данной картой.</span><span class="sxs-lookup"><span data-stu-id="85f72-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="85f72-118">**скардлистреадерграупс**</span><span class="sxs-lookup"><span data-stu-id="85f72-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="85f72-119">Получите список групп читателей, которые ранее появились в системе.</span><span class="sxs-lookup"><span data-stu-id="85f72-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="85f72-120">**скардлистреадерс**</span><span class="sxs-lookup"><span data-stu-id="85f72-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="85f72-121">Получение списка читателей в наборе именованных групп читателей.</span><span class="sxs-lookup"><span data-stu-id="85f72-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 
