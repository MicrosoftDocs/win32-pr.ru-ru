---
description: Управление базой данных смарт-карт и обновлением базы данных с помощью указанного контекста Resource Manager.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Функции управления базами данных смарт-карт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347305"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="1bf7c-103">Функции управления базами данных смарт-карт</span><span class="sxs-lookup"><span data-stu-id="1bf7c-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="1bf7c-104">Следующие функции управляют [*базой данных смарт-карты*](../secgloss/s-gly.md)и обновляют базу данных с помощью указанного [*контекста Resource Manager*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1bf7c-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="1bf7c-105">Безопасность базы данных обеспечивается путем размещения ограничений доступа к базе данных, а не путем добавления механизмов безопасности в [*подсистему смарт-карт*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1bf7c-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="1bf7c-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="1bf7c-106">Topic</span></span>                                                            | <span data-ttu-id="1bf7c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1bf7c-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bf7c-108">**скардаддреадертограуп**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="1bf7c-109">Добавьте [*читателя*](../secgloss/r-gly.md) в [*группу читателей*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1bf7c-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="1bf7c-110">**скардфоржеткардтипе**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="1bf7c-111">Удалите смарт-карту из системы.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="1bf7c-112">**скардфоржетреадер**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="1bf7c-113">Удалите модуль чтения из системы.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="1bf7c-114">**скардфоржетреадерграуп**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="1bf7c-115">Удаление группы читателей из системы.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="1bf7c-116">**скардинтродуцекардтипе**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="1bf7c-117">Ввести новую карточку в систему.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="1bf7c-118">**скардинтродуцереадер**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="1bf7c-119">Познакомьтесь с новым модулем чтения в системе.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="1bf7c-120">**скардинтродуцереадерграуп**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="1bf7c-121">Ввести новую группу читателей в систему.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="1bf7c-122">**скардремовереадерфромграуп**</span><span class="sxs-lookup"><span data-stu-id="1bf7c-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="1bf7c-123">Удаление модуля чтения из группы читателей.</span><span class="sxs-lookup"><span data-stu-id="1bf7c-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 
