---
description: Преобразования, которые не были защищены, как описано в разделе Безопасные преобразования, по умолчанию являются незащищенными.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Незащищенные преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674429"
---
# <a name="unsecured-transforms"></a><span data-ttu-id="410d3-103">Незащищенные преобразования</span><span class="sxs-lookup"><span data-stu-id="410d3-103">Unsecured Transforms</span></span>

<span data-ttu-id="410d3-104">Преобразования, которые не были защищены, как описано в разделе [безопасные преобразования](secured-transforms.md) , по умолчанию являются незащищенными.</span><span class="sxs-lookup"><span data-stu-id="410d3-104">Transforms that have not been secured as described in [Secured Transforms](secured-transforms.md) are unsecured transforms by default.</span></span>

<span data-ttu-id="410d3-105">Чтобы применить незащищенное преобразование при установке пакета, передайте имена файлов преобразования [**в свойство**](transforms.md) Transforms или строку командной строки.</span><span class="sxs-lookup"><span data-stu-id="410d3-105">To apply an unsecured transform when installing a package, pass the transform file names in the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="410d3-106">Не начинайте строку с символами @ или \| задайте [политику трансформссекуре](transformssecure-policy.md) или свойство [**трансформссекуре**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="410d3-106">Do not begin the string with the @ or \| characters or set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="410d3-107">Обратите внимание, что нельзя сочетать незащищенные преобразования и [защищенные преобразования](secured-transforms.md) в одном списке преобразований.</span><span class="sxs-lookup"><span data-stu-id="410d3-107">Note that you cannot combine unsecured transforms and [secured transforms](secured-transforms.md) in the same transforms list.</span></span>

<span data-ttu-id="410d3-108">Если пакет установлен или объявлен в [контексте установки](installation-context.md)для каждого пользователя и имеет незащищенные преобразования, установщик сохраняет источник преобразования в папке Application Data в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="410d3-108">If the package is installed or advertised in the per-user [installation context](installation-context.md), and has unsecured transforms, the installer saves the transform source in the Application Data folder in the user's profile.</span></span> <span data-ttu-id="410d3-109">Это позволяет пользователю поддерживать настройку продукта при перемещении между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="410d3-109">This enables a user to maintain their customization of a product while moving between computers.</span></span>

<span data-ttu-id="410d3-110">Если пакет установлен или объявлен в [контексте установки](installation-context.md)на компьютере и использует незащищенные преобразования, установщик сохранит источник преобразования в папке% WINDIR% \\ Installer.</span><span class="sxs-lookup"><span data-stu-id="410d3-110">If the package is installed or advertised in the per-machine [installation context](installation-context.md), and uses unsecured transforms, the installer saves the transform source in the %windir%\\Installer folder.</span></span>

<span data-ttu-id="410d3-111">Во время первой установки пакета установщик сначала выполняет поиск преобразования в источнике, предоставленном [**свойством Transforms**](transforms.md) или строки командной строки.</span><span class="sxs-lookup"><span data-stu-id="410d3-111">During a first-time installation of the package, the installer first searches for the transform at the source supplied by the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="410d3-112">Если этот источник недоступен, установщик выполняет поиск преобразования в источнике пакета рядом с MSI-файлом.</span><span class="sxs-lookup"><span data-stu-id="410d3-112">If this source is unavailable, the installer then searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="410d3-113">Во время [установки обслуживания](maintenance-installation.md)Установщик выполняет поиск преобразования в расположении кэша.</span><span class="sxs-lookup"><span data-stu-id="410d3-113">During a [maintenance installation](maintenance-installation.md), the installer searches for the transform at the cache location.</span></span> <span data-ttu-id="410d3-114">Если кэшированная копия преобразования становится недоступной, установщик выполняет поиск преобразования в источнике пакета рядом с расширением MSI.</span><span class="sxs-lookup"><span data-stu-id="410d3-114">If the cached copy of the transform becomes unavailable, the installer searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="410d3-115">Дополнительные сведения см. в разделе [применение преобразований](applying-transforms.md) и [отказоустойчивости источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="410d3-115">For more information, see [Applying Transforms](applying-transforms.md) and [Source Resiliency](source-resiliency.md).</span></span>

 

 



