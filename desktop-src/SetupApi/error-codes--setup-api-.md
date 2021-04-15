---
description: Следующие коды ошибок относятся к API установки.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Коды ошибок (API установки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497904"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="a1927-103">Коды ошибок (API установки)</span><span class="sxs-lookup"><span data-stu-id="a1927-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="a1927-104">Следующие коды ошибок относятся к API установки.</span><span class="sxs-lookup"><span data-stu-id="a1927-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="a1927-105">Ошибки разбора INF-файла</span><span class="sxs-lookup"><span data-stu-id="a1927-105">INF Parsing Errors</span></span>              | <span data-ttu-id="a1927-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a1927-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1927-107">Ошибка \_ ожидаемое \_ \_ имя раздела</span><span class="sxs-lookup"><span data-stu-id="a1927-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="a1927-108">Ожидалось имя раздела, и оно не найдено.</span><span class="sxs-lookup"><span data-stu-id="a1927-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="a1927-109">Ошибка \_ неправильной \_ \_ строки имени раздела \_</span><span class="sxs-lookup"><span data-stu-id="a1927-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="a1927-110">Недопустимый формат имени раздела.</span><span class="sxs-lookup"><span data-stu-id="a1927-110">The section name was not of the correct format.</span></span> <span data-ttu-id="a1927-111">(Например, имя, не заканчивающееся правой скобкой ( \] ).</span><span class="sxs-lookup"><span data-stu-id="a1927-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="a1927-112">\_ \_ \_ слишком \_ ДЛИННое имя раздела ошибки</span><span class="sxs-lookup"><span data-stu-id="a1927-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="a1927-113">Длина имени раздела превышает максимальную длину в \_ сект \_ имени \_ Len.</span><span class="sxs-lookup"><span data-stu-id="a1927-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="a1927-114">Ошибка \_ общего \_ синтаксиса</span><span class="sxs-lookup"><span data-stu-id="a1927-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="a1927-115">Неверный общий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="a1927-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="a1927-116">Ошибки времени выполнения INF</span><span class="sxs-lookup"><span data-stu-id="a1927-116">INF Runtime Errors</span></span>         | <span data-ttu-id="a1927-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a1927-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1927-118">ОШИБОЧный \_ \_ \_ Стиль INF</span><span class="sxs-lookup"><span data-stu-id="a1927-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="a1927-119">Тип INF-файла не указан в вызове функции.</span><span class="sxs-lookup"><span data-stu-id="a1927-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="a1927-120">Например, эта ошибка может возвращаться функцией [**сетупопенаппендинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , если INF-файл предназначен для ранних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="a1927-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="a1927-121">\_раздел ошибки \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="a1927-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="a1927-122">Раздел не найден в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="a1927-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="a1927-123">\_строка ошибки \_ не \_ найдена</span><span class="sxs-lookup"><span data-stu-id="a1927-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="a1927-124">Строка не найдена в разделе INF.</span><span class="sxs-lookup"><span data-stu-id="a1927-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



