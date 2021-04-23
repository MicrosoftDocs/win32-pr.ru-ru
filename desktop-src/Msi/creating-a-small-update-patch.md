---
description: При создании исправления для установщик Windows незначительного обновления следуйте приведенным ниже рекомендациям.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Создание небольшого исправления обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664490"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="12b81-103">Создание небольшого исправления обновления</span><span class="sxs-lookup"><span data-stu-id="12b81-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="12b81-104">При создании исправления для [небольших обновлений](small-updates.md)авторы должны следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="12b81-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="12b81-105">Небольшие исправления обновлений должны быть разработаны для одной целевой установки.</span><span class="sxs-lookup"><span data-stu-id="12b81-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="12b81-106">Небольшие исправления обновлений должны использовать самую раннюю версию в качестве целевой установки.</span><span class="sxs-lookup"><span data-stu-id="12b81-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="12b81-107">Небольшое исправление обновления должно заменить и сделать устаревшими все предыдущие обновления незначительных обновлений.</span><span class="sxs-lookup"><span data-stu-id="12b81-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="12b81-108">В следующем сценарии показано, когда лучше использовать небольшое обновление обновления.</span><span class="sxs-lookup"><span data-stu-id="12b81-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="12b81-109">Ваша компания отправляет Myproduct.msi версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="12b81-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="12b81-110">Вскоре после этого вы отправите [небольшое обновление обновления](small-updates.md) для Myproduct.msi с именем QFE1.</span><span class="sxs-lookup"><span data-stu-id="12b81-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="12b81-111">Это не изменяет свойство [**ProductCode**](productcode.md) или свойство [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="12b81-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="12b81-112">Позже вы разпишете второе исправление [обновления](small-updates.md) для Myproduct.msi с именем QFE2.</span><span class="sxs-lookup"><span data-stu-id="12b81-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="12b81-113">Это второе исправление должно быть предназначено для Myproduct.msi версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="12b81-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="12b81-114">Это второе исправление не должно быть предназначено как для Myproduct.msi версии 1,0, так и для Myproduct.msi версии 1,0 + QFE1.</span><span class="sxs-lookup"><span data-stu-id="12b81-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="12b81-115">При применении QFE2 необходимо удалить QFE1.</span><span class="sxs-lookup"><span data-stu-id="12b81-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



