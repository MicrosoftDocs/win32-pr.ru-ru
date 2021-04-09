---
description: Если для этой системной политики на уровне пользователя задано значение &\# 0034; 1&\# 0034;, установщик выполняет поиск файлов преобразования в корне всех сетевых источников в списке источников для продукта. По умолчанию преобразования хранятся в папке Application Data профиля пользователя.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Политика Трансформсатсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143438"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="68d6f-104">Политика Трансформсатсаурце</span><span class="sxs-lookup"><span data-stu-id="68d6f-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="68d6f-105">Если для этой [системной политики](system-policy.md) "на пользователя" задано значение "1"; Установщик выполняет поиск файлов преобразования в корне всех сетевых источников в списке источников для продукта.</span><span class="sxs-lookup"><span data-stu-id="68d6f-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="68d6f-106">По умолчанию преобразования хранятся в папке Application Data профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="68d6f-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="68d6f-107">Установщик Windows интерпретирует политику Трансформсатсаурце как ту же, что и [Политика трансформссекуре](transformssecure-policy.md).</span><span class="sxs-lookup"><span data-stu-id="68d6f-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="68d6f-108">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="68d6f-108">Registry Key</span></span>

<span data-ttu-id="68d6f-109">**HKey \_ Текущие \_ политики пользовательского** \\ **программного обеспечения** \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="68d6f-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="68d6f-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="68d6f-110">Data Type</span></span>

<span data-ttu-id="68d6f-111">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="68d6f-111">**REG\_SZ**</span></span>

 

 



