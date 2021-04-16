---
description: Для управления списком слов, присоединенным к контексту распознавателя, используется обработчик ХРЕКОВОРДЛИСТ. Для улучшения результатов распознавания используется список слов.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: ХРЕКОВОРДЛИСТ (краткий обзор. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542122"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="bcd22-104">ХРЕКОВОРДЛИСТ, обработчик</span><span class="sxs-lookup"><span data-stu-id="bcd22-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="bcd22-105">Для управления списком слов, присоединенным к контексту распознавателя, используется обработчик **хрековордлист** .</span><span class="sxs-lookup"><span data-stu-id="bcd22-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="bcd22-106">Для улучшения результатов распознавания используется список слов.</span><span class="sxs-lookup"><span data-stu-id="bcd22-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="bcd22-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcd22-107">Remarks</span></span>

<span data-ttu-id="bcd22-108">Следующая функция использует **хрековордлист**.</span><span class="sxs-lookup"><span data-stu-id="bcd22-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="bcd22-109">Функция</span><span class="sxs-lookup"><span data-stu-id="bcd22-109">Function</span></span>                                         | <span data-ttu-id="bcd22-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bcd22-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="bcd22-111">**аддвордстовордлист**</span><span class="sxs-lookup"><span data-stu-id="bcd22-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="bcd22-112">Добавляет одно или несколько слов в список слов.</span><span class="sxs-lookup"><span data-stu-id="bcd22-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="bcd22-113">**дестройвордлист**</span><span class="sxs-lookup"><span data-stu-id="bcd22-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="bcd22-114">Уничтожает текущий список слов.</span><span class="sxs-lookup"><span data-stu-id="bcd22-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="bcd22-115">**макевордлист**</span><span class="sxs-lookup"><span data-stu-id="bcd22-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="bcd22-116">Создает список слов.</span><span class="sxs-lookup"><span data-stu-id="bcd22-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="bcd22-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bcd22-117">Requirements</span></span>



| <span data-ttu-id="bcd22-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bcd22-118">Requirement</span></span> | <span data-ttu-id="bcd22-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bcd22-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd22-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcd22-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd22-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bcd22-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="bcd22-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcd22-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd22-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bcd22-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="bcd22-124">Header</span><span class="sxs-lookup"><span data-stu-id="bcd22-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcd22-125"><dt>Напомню. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcd22-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcd22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd22-127">**Функция Сетвордлист**</span><span class="sxs-lookup"><span data-stu-id="bcd22-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




