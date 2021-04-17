---
description: Представляет список слов, которые можно использовать для улучшения результатов распознавания.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Класс Инквордлист (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703053"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="45eae-103">Класс Инквордлист</span><span class="sxs-lookup"><span data-stu-id="45eae-103">InkWordList class</span></span>

<span data-ttu-id="45eae-104">Представляет список слов, которые можно использовать для улучшения результатов распознавания.</span><span class="sxs-lookup"><span data-stu-id="45eae-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="45eae-105">**Инквордлист** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="45eae-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="45eae-106">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="45eae-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="45eae-107">Методы</span><span class="sxs-lookup"><span data-stu-id="45eae-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="45eae-108">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="45eae-108">Interfaces</span></span>

<span data-ttu-id="45eae-109">Класс **инквордлист** определяет эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="45eae-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="45eae-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="45eae-110">Interface</span></span>        | <span data-ttu-id="45eae-111">Описание</span><span class="sxs-lookup"><span data-stu-id="45eae-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="45eae-112">**иинквордлист**</span><span class="sxs-lookup"><span data-stu-id="45eae-112">**IInkWordList**</span></span> | <span data-ttu-id="45eae-113">Этот объект реализует COM-интерфейс **иинквордлист** .</span><span class="sxs-lookup"><span data-stu-id="45eae-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="45eae-114">Методы</span><span class="sxs-lookup"><span data-stu-id="45eae-114">Methods</span></span>

<span data-ttu-id="45eae-115">Класс **инквордлист** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="45eae-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="45eae-116">Метод</span><span class="sxs-lookup"><span data-stu-id="45eae-116">Method</span></span>                                       | <span data-ttu-id="45eae-117">Описание</span><span class="sxs-lookup"><span data-stu-id="45eae-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="45eae-118">**аддворд**</span><span class="sxs-lookup"><span data-stu-id="45eae-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="45eae-119">Добавляет одно слово в **инквордлист**.</span><span class="sxs-lookup"><span data-stu-id="45eae-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="45eae-120">**AutoMerge**</span><span class="sxs-lookup"><span data-stu-id="45eae-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="45eae-121">Выполняет слияние другого **инквордлист** с этим **инквордлист**.</span><span class="sxs-lookup"><span data-stu-id="45eae-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="45eae-122">**ремовеворд**</span><span class="sxs-lookup"><span data-stu-id="45eae-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="45eae-123">Удаляет одно слово из **инквордлист**.</span><span class="sxs-lookup"><span data-stu-id="45eae-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="45eae-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45eae-124">Remarks</span></span>

<span data-ttu-id="45eae-125">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.</span><span class="sxs-lookup"><span data-stu-id="45eae-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="45eae-126">Требования</span><span class="sxs-lookup"><span data-stu-id="45eae-126">Requirements</span></span>



| <span data-ttu-id="45eae-127">Требование</span><span class="sxs-lookup"><span data-stu-id="45eae-127">Requirement</span></span> | <span data-ttu-id="45eae-128">Значение</span><span class="sxs-lookup"><span data-stu-id="45eae-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45eae-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45eae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="45eae-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="45eae-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="45eae-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45eae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="45eae-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="45eae-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="45eae-133">Header</span><span class="sxs-lookup"><span data-stu-id="45eae-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="45eae-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="45eae-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="45eae-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45eae-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="45eae-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45eae-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="45eae-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45eae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45eae-138">**Список слов**</span><span class="sxs-lookup"><span data-stu-id="45eae-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="45eae-139">Константы фактоид</span><span class="sxs-lookup"><span data-stu-id="45eae-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="45eae-140">**Класс Инкрекогнизерконтекст**</span><span class="sxs-lookup"><span data-stu-id="45eae-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

