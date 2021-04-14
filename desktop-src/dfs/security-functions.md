---
title: Функции безопасности
description: Функции безопасности управления сетью получают и устанавливают дескрипторы безопасности для изолированных корней DFS на основе домена и автономных расположений.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496638"
---
# <a name="security-functions"></a><span data-ttu-id="f17b9-103">Функции безопасности</span><span class="sxs-lookup"><span data-stu-id="f17b9-103">Security Functions</span></span>

<span data-ttu-id="f17b9-104">Функции безопасности управления сетью получают и устанавливают дескрипторы безопасности для изолированных корней DFS на основе домена и автономных расположений.</span><span class="sxs-lookup"><span data-stu-id="f17b9-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="f17b9-105">Ниже перечислены функции безопасности DFS.</span><span class="sxs-lookup"><span data-stu-id="f17b9-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="f17b9-106">Функция</span><span class="sxs-lookup"><span data-stu-id="f17b9-106">Function</span></span>                                                               | <span data-ttu-id="f17b9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f17b9-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f17b9-108">**нетдфсжетсекурити**</span><span class="sxs-lookup"><span data-stu-id="f17b9-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="f17b9-109">Получает дескриптор безопасности для корневого объекта указанного корня DFS.</span><span class="sxs-lookup"><span data-stu-id="f17b9-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="f17b9-110">**нетдфссетсекурити**</span><span class="sxs-lookup"><span data-stu-id="f17b9-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="f17b9-111">Находит корневой объект для указанного корня DFS и устанавливает для него указанный дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="f17b9-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="f17b9-112">**нетдфсжетстдконтаинерсекурити**</span><span class="sxs-lookup"><span data-stu-id="f17b9-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="f17b9-113">Получает дескриптор безопасности для объекта контейнера указанного изолированного корневого корня DFS.</span><span class="sxs-lookup"><span data-stu-id="f17b9-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="f17b9-114">**нетдфссетстдконтаинерсекурити**</span><span class="sxs-lookup"><span data-stu-id="f17b9-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="f17b9-115">Находит объект контейнера для указанного автономного корня DFS и устанавливает для него указанный дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="f17b9-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="f17b9-116">**нетдфсжетфтконтаинерсекурити**</span><span class="sxs-lookup"><span data-stu-id="f17b9-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="f17b9-117">Получает дескриптор безопасности для объекта контейнера указанного корня домена DFS.</span><span class="sxs-lookup"><span data-stu-id="f17b9-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="f17b9-118">**нетдфссетфтконтаинерсекурити**</span><span class="sxs-lookup"><span data-stu-id="f17b9-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="f17b9-119">Находит объект контейнера для указанного корня домена DFS и задает для него указанный дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="f17b9-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |
