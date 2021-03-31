---
description: Установка этой системной политики для отдельных пользователей определяет порядок, в котором установщик выполняет поиск трех типов источников.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: сеарчордер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913664"
---
# <a name="searchorder"></a><span data-ttu-id="fba8c-103">сеарчордер</span><span class="sxs-lookup"><span data-stu-id="fba8c-103">SearchOrder</span></span>

<span data-ttu-id="fba8c-104">Установка этой [системной политики](system-policy.md) для отдельных пользователей определяет порядок, в котором установщик выполняет поиск трех типов источников.</span><span class="sxs-lookup"><span data-stu-id="fba8c-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="fba8c-105">Ниже приведены типы источников.</span><span class="sxs-lookup"><span data-stu-id="fba8c-105">The types of sources are:</span></span>

<span data-ttu-id="fba8c-106">"n" — сеть</span><span class="sxs-lookup"><span data-stu-id="fba8c-106">"n" – network</span></span>

<span data-ttu-id="fba8c-107">"m" — носитель (компакт-диск или DVD-диск)</span><span class="sxs-lookup"><span data-stu-id="fba8c-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="fba8c-108">"u" — универсальный указатель ресурсов (URL-адрес)</span><span class="sxs-lookup"><span data-stu-id="fba8c-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="fba8c-109">Например, для поиска сетевых источников в первую очередь, источники мультимедиа Second и URL-адреса последними устанавливают для этой политики значение "НМУ".</span><span class="sxs-lookup"><span data-stu-id="fba8c-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="fba8c-110">Чтобы пропустить Поиск конкретного типа источника, оставьте соответствующую букву из значения.</span><span class="sxs-lookup"><span data-stu-id="fba8c-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="fba8c-111">Если Сеарчордер не задан, то по умолчанию используется порядок поиска Network, Media, а затем URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="fba8c-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fba8c-112">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="fba8c-112">Registry Key</span></span>

<span data-ttu-id="fba8c-113">**HKey \_ Текущие \_ политики пользовательского** \\ **программного обеспечения** \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="fba8c-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="fba8c-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fba8c-114">Data Type</span></span>

<span data-ttu-id="fba8c-115">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fba8c-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="fba8c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fba8c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fba8c-117">Отказоустойчивость источника</span><span class="sxs-lookup"><span data-stu-id="fba8c-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



