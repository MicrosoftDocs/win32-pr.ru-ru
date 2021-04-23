---
description: Для NLS Сортировка (также известная как &\# 0034; параметры сортировки&\# 0034;) — Это упорядочение строк.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Сортировка (Международная связь)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272809"
---
# <a name="sorting"></a><span data-ttu-id="920b3-103">Сортировка</span><span class="sxs-lookup"><span data-stu-id="920b3-103">Sorting</span></span>

<span data-ttu-id="920b3-104">Для NLS Сортировка (также называемая "параметрами сортировки") представляет собой расположение строк.</span><span class="sxs-lookup"><span data-stu-id="920b3-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="920b3-105">Существует два типа сортировки:</span><span class="sxs-lookup"><span data-stu-id="920b3-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="920b3-106">Лингвистическая сортировка.</span><span class="sxs-lookup"><span data-stu-id="920b3-106">Linguistic sorting.</span></span> <span data-ttu-id="920b3-107">Упорядочивает строки с похожими лингвистическими характеристиками в группы (по сортировке).</span><span class="sxs-lookup"><span data-stu-id="920b3-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="920b3-108">Порядковые (не лингвистические) сортировки.</span><span class="sxs-lookup"><span data-stu-id="920b3-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="920b3-109">Упорядочивает строки в упорядоченной последовательности.</span><span class="sxs-lookup"><span data-stu-id="920b3-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="920b3-110">При сортировке используются функции сравнения строк NLS, такие как [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) и [**LCMapString завершилось ошибкой**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), или функции API-оболочки, такие как [лстркмп](/windows/win32/api/winbase/nf-winbase-lstrcmpa), которые внутренне вызывают функции сравнения строк NLS.</span><span class="sxs-lookup"><span data-stu-id="920b3-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="920b3-111">Дополнительные сведения о реализации сортировки в приложениях см. [в разделе Обработка сортировки в приложениях](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="920b3-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="920b3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="920b3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920b3-113">Сведения о поддержке национальных языков</span><span class="sxs-lookup"><span data-stu-id="920b3-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="920b3-114">Обработка сортировки в приложениях</span><span class="sxs-lookup"><span data-stu-id="920b3-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="920b3-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="920b3-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="920b3-116">LCMapString завершилось ошибкой</span><span class="sxs-lookup"><span data-stu-id="920b3-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
