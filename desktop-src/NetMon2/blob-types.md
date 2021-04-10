---
description: Сетевой монитор использует три типа больших двоичных объектов (BLOB) для выбора и подключения сетевых карт, сбора данных и управления данными НПП.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Типы больших двоичных объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272598"
---
# <a name="blob-types"></a><span data-ttu-id="1c4a7-103">Типы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="1c4a7-103">BLOB Types</span></span>

<span data-ttu-id="1c4a7-104">Сетевой монитор использует три типа больших двоичных объектов (BLOB) для выбора и подключения сетевых карт, сбора данных и управления данными НПП.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="1c4a7-105">БОЛЬШОЙ ДВОИЧНЫЙ ОБЪЕКТ НПП</span><span class="sxs-lookup"><span data-stu-id="1c4a7-105">NPP BLOB</span></span>

<span data-ttu-id="1c4a7-106">Приложения используют большие двоичные объекты НПП для подключения к определенной сетевой карте через НПП.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="1c4a7-107">(Приложение устанавливает соединение с вызовом **креатенппинтерфаце** и данными о расположении в большом ДВОИЧНОМ объекте НПП.) Приложение также может хранить свои данные конфигурации в большом двоичном объекте НПП, чтобы настроить НПП.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="1c4a7-108">Кроме того, приложение, сохраняющее большой двоичный объект НПП, не обязательно должно проходить через поиск для повторного использования этого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="1c4a7-109">Фильтровать большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="1c4a7-109">Filter BLOB</span></span>

<span data-ttu-id="1c4a7-110">Большой двоичный объект фильтра содержит определяемые приложением условия, которые можно использовать для выбора НПП и сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="1c4a7-111">Например, приложение может запросить определенную сетевую карту, только карты Ethernet или карты, поддерживающие конкретный темп записи кадров.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="1c4a7-112">Специальный большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="1c4a7-112">Special BLOB</span></span>

<span data-ttu-id="1c4a7-113">Если НПП требует дополнительных данных, прежде чем он сможет вернуть НПП большой двоичный объект в приложение, НПП использует специальный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="1c4a7-114">Чаще всего приложению не требуются или не используются специальные большие двоичные объекты, поэтому они не возвращаются в приложение, если в одном вызове функции не задан определенный флаг.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="1c4a7-115">Например, удаленный НПП использует специальный большой двоичный объект, так как для создания соединения требуется имя пути.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="1c4a7-116">Приложение, которое получает удаленный Специальный большой двоичный объект НПП, может добавить строку и выполнить обратный вызов в Finder для получения таблицы BLOB-объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="1c4a7-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="1c4a7-117">Дополнительные сведения см. в разделе [специальные записи большого двоичного объекта](special-blob-entries.md).</span><span class="sxs-lookup"><span data-stu-id="1c4a7-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



