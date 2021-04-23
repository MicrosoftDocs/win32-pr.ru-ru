---
description: '\_Описание константы языкового стандарта иконструктедлокале'
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/30/2021
ms.locfileid: "105995144"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="6dc7d-103">иконструктедлокале ЛОКАЛи \_</span><span class="sxs-lookup"><span data-stu-id="6dc7d-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="6dc7d-104">Идентификатор для запроса, если языковой стандарт — "сконструированный" языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="6dc7d-105">Использовать этот LCTYPE не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="6dc7d-106">Это определяет языковой стандарт, для которого у Windows много нет полных сведений, и они должны "формироваться" информацию во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="6dc7d-107">Обычно сведения, предоставляемые LOCALE_ICONSTRUCTEDLOCALE, имеют ограниченный объем использования, так как Windows предоставляет столько данных, сколько доступно для каждого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="6dc7d-108">Поэтому использовать этот LCTYPE не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="6dc7d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6dc7d-109">Value</span></span> | <span data-ttu-id="6dc7d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6dc7d-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="6dc7d-111">0</span><span class="sxs-lookup"><span data-stu-id="6dc7d-111">0</span></span>     | <span data-ttu-id="6dc7d-112">Не создано</span><span class="sxs-lookup"><span data-stu-id="6dc7d-112">Not constructed</span></span>         |
| <span data-ttu-id="6dc7d-113">1</span><span class="sxs-lookup"><span data-stu-id="6dc7d-113">1</span></span>     | <span data-ttu-id="6dc7d-114">Является сконструированным языковым стандартом</span><span class="sxs-lookup"><span data-stu-id="6dc7d-114">Is a constructed locale</span></span> |


<span data-ttu-id="6dc7d-115">Примером может быть запрос "de-US" или немецкий в США.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="6dc7d-116">NLS будет использовать данные на немецком языке, которые он может найти, а также данные США региона, которые она может найти.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="6dc7d-117">Это может быть не так, как, например, система, скорее всего, не будет содержать сведения об имени США на немецком языке.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="6dc7d-118">Однако если приложение или пользователь помещает контекст "de-US", то возвращаемые данные лучше доступны.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="6dc7d-119">Приложения, использующие LOCALE_ICONSTRUCTEDLOCALE для отклонения национальных настроек и переходят на другой языковой стандарт, обычно в конечном итоге имеют более серьезную работу, например, в нашем примере — de-DE или EN-US.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="6dc7d-120">Ни один из них не близок к исходному запросу немецкого языка с СШАным регионом.</span><span class="sxs-lookup"><span data-stu-id="6dc7d-120">Neither of those are close to the original request for German language with a United States region.</span></span>

