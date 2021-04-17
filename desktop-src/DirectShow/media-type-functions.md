---
description: Базовые классы DirectShow предоставляют вспомогательные функции для обработки \_ структуры типа мультимедиа AM \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Функции типа мультимедиа (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685046"
---
# <a name="media-type-functions"></a><span data-ttu-id="5ed49-103">Функции типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="5ed49-103">Media Type Functions</span></span>

<span data-ttu-id="5ed49-104">Базовые классы DirectShow предоставляют вспомогательные функции для обработки структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5ed49-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="5ed49-105">Структура **\_ \_ типа мультимедиа AM** содержит указатель (элемент **пбформат** ) на другой блок памяти, который называется *блоком формата*.</span><span class="sxs-lookup"><span data-stu-id="5ed49-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="5ed49-106">Поэтому при работе с этой структурой необходимо соблюдать осторожность при выделении памяти, чтобы избежать утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="5ed49-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="5ed49-107">Память выделяется следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="5ed49-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="5ed49-108">**Креатемедиатипе** выделяет новую структуру **\_ \_ типа мультимедиа AM** и блок Format.</span><span class="sxs-lookup"><span data-stu-id="5ed49-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="5ed49-109">**Копимедиатипе** копирует в существующую структуру **\_ \_ типа мультимедиа AM** , но выделяет блок формата.</span><span class="sxs-lookup"><span data-stu-id="5ed49-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="5ed49-110">**Креатеаудиомедиатипе** инициализирует существующую структуру **\_ \_ типа мультимедиа AM** и при необходимости выделяет блок формата.</span><span class="sxs-lookup"><span data-stu-id="5ed49-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="5ed49-111">Следующие функции освобождают память:</span><span class="sxs-lookup"><span data-stu-id="5ed49-111">The following functions free memory:</span></span>

-   <span data-ttu-id="5ed49-112">**Фримедиатипе** освобождает блок формата.</span><span class="sxs-lookup"><span data-stu-id="5ed49-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="5ed49-113">**Делетемедиатипе** освобождает структуру **\_ \_ типа мультимедиа AM** , включая блок Format.</span><span class="sxs-lookup"><span data-stu-id="5ed49-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="5ed49-114">Функция</span><span class="sxs-lookup"><span data-stu-id="5ed49-114">Function</span></span>                                             | <span data-ttu-id="5ed49-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5ed49-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ed49-116">**копимедиатипе**</span><span class="sxs-lookup"><span data-stu-id="5ed49-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="5ed49-117">Копирует структуру **\_ \_ типа мультимедиа** с выделенной задачей.</span><span class="sxs-lookup"><span data-stu-id="5ed49-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="5ed49-118">**креатеаудиомедиатипе**</span><span class="sxs-lookup"><span data-stu-id="5ed49-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="5ed49-119">Инициализирует структуру типа мультимедиа по структуре звукового формата.</span><span class="sxs-lookup"><span data-stu-id="5ed49-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="5ed49-120">**креатемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="5ed49-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="5ed49-121">Выделяет и инициализирует структуру **\_ \_ типа файлов мультимедиа AM** из существующей структуры **\_ \_ типа мультимедиа AM** .</span><span class="sxs-lookup"><span data-stu-id="5ed49-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="5ed49-122">**делетемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="5ed49-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="5ed49-123">Удаляет структуру **\_ \_ типа мультимедиа** с выделенной задачей.</span><span class="sxs-lookup"><span data-stu-id="5ed49-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="5ed49-124">**фримедиатипе**</span><span class="sxs-lookup"><span data-stu-id="5ed49-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="5ed49-125">Освобождает структуру **\_ \_ типа мультимедиа** , выделенную задачей, из памяти.</span><span class="sxs-lookup"><span data-stu-id="5ed49-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="5ed49-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5ed49-126">Requirements</span></span>



| <span data-ttu-id="5ed49-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5ed49-127">Requirement</span></span> | <span data-ttu-id="5ed49-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5ed49-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed49-129">Header</span><span class="sxs-lookup"><span data-stu-id="5ed49-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5ed49-130"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ed49-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5ed49-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ed49-131">Library</span></span><br/> | <dl> <span data-ttu-id="5ed49-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5ed49-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




