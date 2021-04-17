---
description: Обрабатывает слова, определяемые пределами слов, во время индексирования и во время выполнения запроса.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Интерфейс Ивордсинк (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692180"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="65f69-103">Интерфейс Ивордсинк</span><span class="sxs-lookup"><span data-stu-id="65f69-103">IWordSink interface</span></span>

<span data-ttu-id="65f69-104">Обрабатывает слова, определяемые пределами слов, во время индексирования и во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="65f69-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="65f69-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="65f69-105">Members</span></span>

<span data-ttu-id="65f69-106">Интерфейс **ивордсинк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="65f69-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="65f69-107">**Ивордсинк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65f69-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="65f69-108">Методы</span><span class="sxs-lookup"><span data-stu-id="65f69-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65f69-109">Методы</span><span class="sxs-lookup"><span data-stu-id="65f69-109">Methods</span></span>

<span data-ttu-id="65f69-110">Интерфейс **ивордсинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="65f69-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="65f69-111">Метод</span><span class="sxs-lookup"><span data-stu-id="65f69-111">Method</span></span>                                             | <span data-ttu-id="65f69-112">Описание</span><span class="sxs-lookup"><span data-stu-id="65f69-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65f69-113">**ендалтфрасе**</span><span class="sxs-lookup"><span data-stu-id="65f69-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="65f69-114">Указывает конец конечной фразы в последовательности альтернативных фраз, формируемых средством разбиения по словам во время индексирования.</span><span class="sxs-lookup"><span data-stu-id="65f69-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="65f69-115">**путалтворд**</span><span class="sxs-lookup"><span data-stu-id="65f69-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="65f69-116">Помещает в объект **ивордсинк** альтернативное слово и его расположение.</span><span class="sxs-lookup"><span data-stu-id="65f69-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="65f69-117">**путбреак**</span><span class="sxs-lookup"><span data-stu-id="65f69-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="65f69-118">Помещает разрыв после предыдущего слова.</span><span class="sxs-lookup"><span data-stu-id="65f69-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="65f69-119">**путворд**</span><span class="sxs-lookup"><span data-stu-id="65f69-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="65f69-120">Помещает слово и его расположение в объекте **ивордсинк** .</span><span class="sxs-lookup"><span data-stu-id="65f69-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="65f69-121">**старталтфрасе**</span><span class="sxs-lookup"><span data-stu-id="65f69-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="65f69-122">Указывает границу между фразами в последовательности альтернативных фраз, формируемых средством разбиения по словам во время индексирования.</span><span class="sxs-lookup"><span data-stu-id="65f69-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65f69-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65f69-123">Remarks</span></span>

<span data-ttu-id="65f69-124">Поиск Windows создает и инициализирует экземпляры объекта **ивордсинк** .</span><span class="sxs-lookup"><span data-stu-id="65f69-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="65f69-125">Объект **ивордсинк** получает параметр *фкуери* во время инициализации и использует этот параметр для определения контекста разбиения по словам, в котором используется объект.</span><span class="sxs-lookup"><span data-stu-id="65f69-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="65f69-126">Реализации [**ивордбреакер**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) получают указатель на объект **ивордсинк** в методе [**ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="65f69-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f69-127">Требования</span><span class="sxs-lookup"><span data-stu-id="65f69-127">Requirements</span></span>



| <span data-ttu-id="65f69-128">Требование</span><span class="sxs-lookup"><span data-stu-id="65f69-128">Requirement</span></span> | <span data-ttu-id="65f69-129">Значение</span><span class="sxs-lookup"><span data-stu-id="65f69-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65f69-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65f69-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65f69-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65f69-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="65f69-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65f69-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65f69-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65f69-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65f69-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65f69-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f69-135"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="65f69-135"><dt>Search.h</dt></span></span> </dl> |



 

 
