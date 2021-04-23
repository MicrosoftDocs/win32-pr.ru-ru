---
description: Указывает границу между фразами в последовательности альтернативных фраз, формируемых средством разбиения по словам во время индексирования.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Метод Ивордсинк:: Старталтфрасе (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262926"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="e20fb-103">Метод Ивордсинк:: Старталтфрасе</span><span class="sxs-lookup"><span data-stu-id="e20fb-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="e20fb-104">Указывает границу между фразами в последовательности альтернативных фраз, формируемых средством разбиения по словам во время индексирования.</span><span class="sxs-lookup"><span data-stu-id="e20fb-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e20fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e20fb-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="e20fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e20fb-106">Parameters</span></span>

<span data-ttu-id="e20fb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e20fb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e20fb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e20fb-108">Return value</span></span>

<span data-ttu-id="e20fb-109">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e20fb-109">This method can return one of these values.</span></span>



| <span data-ttu-id="e20fb-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e20fb-110">Return code</span></span>                                                                                           | <span data-ttu-id="e20fb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e20fb-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e20fb-112"><dt>**ВБРЕАК \_ \_ только запрос \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="e20fb-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="e20fb-113">[**Старталтфрасе**](iwordsink-startaltphrase.md) вызывается во время запроса.</span><span class="sxs-lookup"><span data-stu-id="e20fb-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e20fb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e20fb-114">Remarks</span></span>

<span data-ttu-id="e20fb-115">Каждая альтернативная фраза начинается с вызова **старталтфрасе** .</span><span class="sxs-lookup"><span data-stu-id="e20fb-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="e20fb-116">Фраза помещается в объект [**ивордсинк**](iwordsink.md) посредством последующих вызовов метода [**Ивордсинк::P утворд**](iwordsink-putword.md) или [**ивордсинк::P уталтворд**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="e20fb-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="e20fb-117">Последняя альтернативная фраза в последовательности фраз завершается вызовом метода [**ивордсинк:: ендалтфрасе**](iwordsink-endaltphrase.md) .</span><span class="sxs-lookup"><span data-stu-id="e20fb-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e20fb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e20fb-118">Requirements</span></span>



| <span data-ttu-id="e20fb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e20fb-119">Requirement</span></span> | <span data-ttu-id="e20fb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e20fb-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e20fb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e20fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e20fb-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e20fb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e20fb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e20fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e20fb-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e20fb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e20fb-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e20fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20fb-126"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20fb-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20fb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e20fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20fb-128">**ивордсинк**</span><span class="sxs-lookup"><span data-stu-id="e20fb-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




