---
title: База данных службы имен RPC
description: Служба имен — это служба, которая сопоставляет имена с объектами и обычно поддерживает пары (имя, объект) в базе данных.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Удаленный вызов процедур RPC, описание, имя базы данных службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486873"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="a8f94-104">База данных службы имен RPC</span><span class="sxs-lookup"><span data-stu-id="a8f94-104">The RPC Name Service Database</span></span>

<span data-ttu-id="a8f94-105">Служба имен — это служба, которая сопоставляет имена с объектами и обычно поддерживает пары (имя, объект) в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a8f94-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="a8f94-106">Как правило, имя — это логическое имя, которое пользователи легко запомнить и использовать.</span><span class="sxs-lookup"><span data-stu-id="a8f94-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="a8f94-107">Например, служба имен позволит пользователю использовать логическое имя "ласерпринтер".</span><span class="sxs-lookup"><span data-stu-id="a8f94-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="a8f94-108">Служба имен сопоставляет это имя с сетевым именем, используемым сервером печати.</span><span class="sxs-lookup"><span data-stu-id="a8f94-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="a8f94-109">Чтобы использовать упрощенное объяснение, служба имен RPC сопоставляет имя с обработчиком привязки и поддерживает сопоставления (имя, маркер привязки) в базе данных службы имен RPC.</span><span class="sxs-lookup"><span data-stu-id="a8f94-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="a8f94-110">Служба имен RPC позволяет клиентским приложениям использовать логическое имя вместо определенной последовательности протокола и сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="a8f94-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="a8f94-111">Использование логического имени упрощает для сетевых администраторов установку и настройку распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="a8f94-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="a8f94-112">Запись базы данных службы имен RPC имеет один из следующих атрибутов: **Server**, **Group** или **Profile**.</span><span class="sxs-lookup"><span data-stu-id="a8f94-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="a8f94-113">В реализации Майкрософт записи могут иметь только один атрибут, поэтому эти записи также называются записями сервера, записями групп и записями профиля.</span><span class="sxs-lookup"><span data-stu-id="a8f94-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="a8f94-114">Запись Server состоит из идентификаторов UUID интерфейса, ИДЕНТИФИКАТОРов объектов (требуется, когда сервер реализует несколько точек входа), сетевой адрес, последовательность протокола и сведения о конечной точке, связанные с известными конечными точками.</span><span class="sxs-lookup"><span data-stu-id="a8f94-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="a8f94-115">При использовании динамической конечной точки сведения о конечной точке хранятся в базе данных-сопоставлении конечной точки, а не в базе данных службы имен, а конечная точка разрешается как любая другая динамическая конечная точка.</span><span class="sxs-lookup"><span data-stu-id="a8f94-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="a8f94-116">Записи сервера управляются функциями, которые начинаются с префикса "Рпкнсбиндинг".</span><span class="sxs-lookup"><span data-stu-id="a8f94-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="a8f94-117">Запись группы может содержать записи сервера или другие записи группы.</span><span class="sxs-lookup"><span data-stu-id="a8f94-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="a8f94-118">Записи группы управляются функциями, которые начинаются с префикса "Рпкнсграуп".</span><span class="sxs-lookup"><span data-stu-id="a8f94-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="a8f94-119">Запись профиля может содержать записи профиля, группы или сервера.</span><span class="sxs-lookup"><span data-stu-id="a8f94-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="a8f94-120">Записи профиля управляются функциями, которые начинаются с префикса "Рпкнспрофиле".</span><span class="sxs-lookup"><span data-stu-id="a8f94-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="a8f94-121">В этом разделе представлен обзор базы данных службы имен в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a8f94-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="a8f94-122">Рекомендации по именам приложений службы</span><span class="sxs-lookup"><span data-stu-id="a8f94-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="a8f94-123">Обзор записи службы имен</span><span class="sxs-lookup"><span data-stu-id="a8f94-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="a8f94-124">Критерии для записей службы имен</span><span class="sxs-lookup"><span data-stu-id="a8f94-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="a8f94-125">Очистка записи службы имен</span><span class="sxs-lookup"><span data-stu-id="a8f94-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="a8f94-126">Что происходит во время запроса</span><span class="sxs-lookup"><span data-stu-id="a8f94-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="a8f94-127">Использование локатора Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a8f94-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="a8f94-128">Использование службы каталогов ячеек (компакт-дисков)</span><span class="sxs-lookup"><span data-stu-id="a8f94-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="a8f94-129">Синтаксис имени</span><span class="sxs-lookup"><span data-stu-id="a8f94-129">Name Syntax</span></span>](name-syntax.md)

 

 




