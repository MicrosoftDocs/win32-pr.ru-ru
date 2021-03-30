---
title: Реализация набора свойств сводных данных
description: При реализации набора свойств сводных данных для структурированного хранилища необходимо следовать рекомендациям.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Реализация набора свойств сводных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772836"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="583ce-104">Реализация набора свойств сводных данных</span><span class="sxs-lookup"><span data-stu-id="583ce-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="583ce-105">При реализации набора свойств сводных данных для структурированного хранилища необходимо следовать рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="583ce-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="583ce-106">Ниже приведены рекомендации по реализации [набора свойств сводных данных](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="583ce-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="583ce-107">**Идентификатор процесса \_ ШАБЛОН** ссылается на внешний документ, содержащий сведения о формате и стиле.</span><span class="sxs-lookup"><span data-stu-id="583ce-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="583ce-108">Процесс, по которому расположен шаблон, определяется реализацией.</span><span class="sxs-lookup"><span data-stu-id="583ce-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="583ce-109">**Идентификатор процесса \_ ЛАСТАУСОР** — это имя, хранящееся в сведениях о пользователе приложением.</span><span class="sxs-lookup"><span data-stu-id="583ce-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="583ce-110">Например, Мария создает документ на своем компьютере и передает ему Джон, который затем изменяет и сохраняет его.</span><span class="sxs-lookup"><span data-stu-id="583ce-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="583ce-111">Мария является автором, а Джон — последним сохраненным по значению.</span><span class="sxs-lookup"><span data-stu-id="583ce-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="583ce-112">**Идентификатор процесса \_ РЕВНУМБЕР** — число вызовов команды File/Save в этом документе.</span><span class="sxs-lookup"><span data-stu-id="583ce-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="583ce-113">Каждое из значений даты и времени должно храниться в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="583ce-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="583ce-114">**Идентификатор процесса \_ CREATE \_ DTM** — это свойство, доступное только для чтения; Это свойство должно быть задано при создании документа, но не должно изменяться впоследствии.</span><span class="sxs-lookup"><span data-stu-id="583ce-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="583ce-115">Для **\_ эскиза PID** приложения должны хранить данные в формате **CF \_ DIB** или **CF \_ метафилепикт** .</span><span class="sxs-lookup"><span data-stu-id="583ce-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="583ce-116">**CF \_** Рекомендуется использовать метафилепикт.</span><span class="sxs-lookup"><span data-stu-id="583ce-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="583ce-117">**Идентификатор процесса \_ БЕЗОПАСНОСТЬ** — это рекомендуемый уровень безопасности для документа.</span><span class="sxs-lookup"><span data-stu-id="583ce-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="583ce-118">Отметив уровень безопасности в документе, приложение, отличное от создателя документа, может изменить его пользовательский интерфейс на свойства.</span><span class="sxs-lookup"><span data-stu-id="583ce-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="583ce-119">Приложение не должно отображать сведения о документе, защищенном паролем, или вносить изменения в принудительные Read-Only или заблокированные документы для заметок.</span><span class="sxs-lookup"><span data-stu-id="583ce-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="583ce-120">Если пользователь пытается изменить свойства, приложение должно предупредить пользователя о том, что Read-Only рекомендуемое состояние.</span><span class="sxs-lookup"><span data-stu-id="583ce-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="583ce-121">Уровень безопасности</span><span class="sxs-lookup"><span data-stu-id="583ce-121">Security level</span></span>         | <span data-ttu-id="583ce-122">Значение</span><span class="sxs-lookup"><span data-stu-id="583ce-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="583ce-123">None</span><span class="sxs-lookup"><span data-stu-id="583ce-123">None</span></span>                   | <span data-ttu-id="583ce-124">0</span><span class="sxs-lookup"><span data-stu-id="583ce-124">0</span></span>     |
| <span data-ttu-id="583ce-125">Защищен паролем</span><span class="sxs-lookup"><span data-stu-id="583ce-125">Password protected</span></span>     | <span data-ttu-id="583ce-126">1</span><span class="sxs-lookup"><span data-stu-id="583ce-126">1</span></span>     |
| <span data-ttu-id="583ce-127">Рекомендуется только для чтения</span><span class="sxs-lookup"><span data-stu-id="583ce-127">Read-only recommended</span></span>  | <span data-ttu-id="583ce-128">2</span><span class="sxs-lookup"><span data-stu-id="583ce-128">2</span></span>     |
| <span data-ttu-id="583ce-129">Принудительно применяется только для чтения</span><span class="sxs-lookup"><span data-stu-id="583ce-129">Read-only enforced</span></span>     | <span data-ttu-id="583ce-130">4</span><span class="sxs-lookup"><span data-stu-id="583ce-130">4</span></span>     |
| <span data-ttu-id="583ce-131">Заблокировано для заметок</span><span class="sxs-lookup"><span data-stu-id="583ce-131">Locked for annotations</span></span> | <span data-ttu-id="583ce-132">8</span><span class="sxs-lookup"><span data-stu-id="583ce-132">8</span></span>     |



 

 

 




