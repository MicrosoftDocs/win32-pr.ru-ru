---
description: Указывает конец конечной фразы в последовательности альтернативных фраз, формируемых средством разбиения по словам во время индексирования.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Метод Ивордсинк:: Ендалтфрасе (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262927"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="2e7b5-103">Метод Ивордсинк:: Ендалтфрасе</span><span class="sxs-lookup"><span data-stu-id="2e7b5-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="2e7b5-104">Указывает конец конечной фразы в последовательности альтернативных фраз, формируемых средством разбиения по словам во время индексирования.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e7b5-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="2e7b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e7b5-106">Parameters</span></span>

<span data-ttu-id="2e7b5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e7b5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e7b5-108">Return value</span></span>

<span data-ttu-id="2e7b5-109">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-109">This method can return one of these values.</span></span>



| <span data-ttu-id="2e7b5-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2e7b5-110">Return code</span></span>                                                                                           | <span data-ttu-id="2e7b5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2e7b5-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e7b5-112"><dt>**ВБРЕАК \_ \_ только запрос \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="2e7b5-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="2e7b5-113">[**Ендалтфрасе**](iwordsink-endaltphrase.md) вызывается во время запроса.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e7b5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e7b5-114">Remarks</span></span>

<span data-ttu-id="2e7b5-115">Реализации [**ивордбреакер**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) вызывают **Ивордсинк:: Ендалтфрасе** из метода [**ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , чтобы завершить последовательность альтернативных фраз.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="2e7b5-116">Метод [**ивордсинк:: старталтфрасе**](iwordsink-startaltphrase.md) вызывается для обозначения конца одной фразы и начала другой в последовательности фраз.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="2e7b5-117">Только последняя фраза в последовательности завершается вызовом **ендалтфрасе**.</span><span class="sxs-lookup"><span data-stu-id="2e7b5-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7b5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e7b5-118">Requirements</span></span>



| <span data-ttu-id="2e7b5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2e7b5-119">Requirement</span></span> | <span data-ttu-id="2e7b5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2e7b5-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7b5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e7b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7b5-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e7b5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2e7b5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e7b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7b5-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e7b5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2e7b5-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2e7b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e7b5-126"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e7b5-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7b5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e7b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7b5-128">**ивордсинк**</span><span class="sxs-lookup"><span data-stu-id="2e7b5-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
