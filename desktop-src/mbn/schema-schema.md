---
description: Определяет профиль мобильного широкополосного подключения.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Справочник по схеме профиля мобильного широкополосного подключения
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662410"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="fbf2a-103">Справочник по схеме профиля мобильного широкополосного подключения</span><span class="sxs-lookup"><span data-stu-id="fbf2a-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="fbf2a-104">Схема профиля мобильного широкополосного подключения определяет профиль мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="fbf2a-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="fbf2a-105">Профили хранят параметры конфигурации пользователя и сети, связанные с мобильным широкополосным подключением.</span><span class="sxs-lookup"><span data-stu-id="fbf2a-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="fbf2a-106">Они также сохраняют настройки пользователя для подключения.</span><span class="sxs-lookup"><span data-stu-id="fbf2a-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="fbf2a-107">Корневым элементом профиля мобильного широкополосного подключения является элемент [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf2a-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="fbf2a-108">Каждый профиль имеет только один корневой элемент.</span><span class="sxs-lookup"><span data-stu-id="fbf2a-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="fbf2a-109">Все элементы схемы профиля мобильной широкополосной связи, используемые Windows 7, находятся в пространстве имен, `https://www.microsoft.com/networking/WWAN/profile/v1` а элементы, используемые Windows 8, находятся в пространстве имен `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="fbf2a-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="fbf2a-110">Схема профиля мобильного широкополосного подключения строго обеспечивает порядок узлов.</span><span class="sxs-lookup"><span data-stu-id="fbf2a-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="fbf2a-111">Узлы, указанные в профиле, должны соответствовать **схеме профиля мобильного широкополосного подключения** и отображаться в порядке, указанном в определении схемы.</span><span class="sxs-lookup"><span data-stu-id="fbf2a-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="fbf2a-112">Например, [**усерлогонкред**](schema-userlogoncred-contexttype-element.md) должен быть указан сразу после [**акцессстринг**](schema-accessstring-contexttype-element.md).</span><span class="sxs-lookup"><span data-stu-id="fbf2a-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="fbf2a-113">Схема профиля мобильного широкополосного подключения v1</span><span class="sxs-lookup"><span data-stu-id="fbf2a-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="fbf2a-114">Схема профиля мобильного широкополосного подключения v2</span><span class="sxs-lookup"><span data-stu-id="fbf2a-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="fbf2a-115">Схема профиля мобильного широкополосного подключения v3</span><span class="sxs-lookup"><span data-stu-id="fbf2a-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="fbf2a-116">[Схема профиля мобильного широкополосного подключения v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fbf2a-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
