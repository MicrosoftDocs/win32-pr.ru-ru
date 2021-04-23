---
description: Помещает слово и его расположение в объекте Ивордсинк.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: 'Ивордсинк: метод:P Утворд (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692181"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="0f284-103">Ивордсинк: метод:P Утворд</span><span class="sxs-lookup"><span data-stu-id="0f284-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="0f284-104">Помещает слово и его расположение в объекте [**ивордсинк**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="0f284-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f284-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f284-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="0f284-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f284-107">*КВК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f284-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f284-108">Число символов в *пвЦинбуф*.</span><span class="sxs-lookup"><span data-stu-id="0f284-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="0f284-109">*пвЦинбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f284-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f284-110">Указатель на буфер, содержащий альтернативную форму слова из исходного текста.</span><span class="sxs-lookup"><span data-stu-id="0f284-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="0f284-111">Этот параметр не изменяется **путворд**.</span><span class="sxs-lookup"><span data-stu-id="0f284-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="0f284-112">При необходимости можно передать параметр *птекстсаурце* из [**Ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="0f284-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="0f284-113">*квксрклен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f284-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f284-114">Количество символов в исходном текстовом буфере (обозначенное параметром *птекстсаурце* в [**Ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)), соответствующее слову, содержащемуся в *пвЦинбуф*.</span><span class="sxs-lookup"><span data-stu-id="0f284-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="0f284-115">*квксркпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f284-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f284-116">Начальное расположение слова в *пвЦинбуф* в исходном текстовом буфере (указывается параметром *птекстсаурце* в [**ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="0f284-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f284-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f284-117">Return value</span></span>

<span data-ttu-id="0f284-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0f284-118">This method can return one of these values.</span></span>



| <span data-ttu-id="0f284-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0f284-119">Return code</span></span>                                                                                              | <span data-ttu-id="0f284-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0f284-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f284-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0f284-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="0f284-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="0f284-122">The operation was completed successfully.</span></span> <span data-ttu-id="0f284-123">Также указывает, что больше нет доступных текста для заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="0f284-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="0f284-124"><dt>**Языковая \_ \_крупное \_ слово S**</dt></span><span class="sxs-lookup"><span data-stu-id="0f284-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="0f284-125">Значение *КВК* больше, чем значение *улмакстокенсизе* , указанное в [**ивордбреакер:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="0f284-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f284-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f284-126">Remarks</span></span>

<span data-ttu-id="0f284-127">Рекомендуется, чтобы метод **ивордсинк::P утворд** всегда содержал исходное слово, как найдено в *птекстсаурце*.</span><span class="sxs-lookup"><span data-stu-id="0f284-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="0f284-128">Альтернативные формы слова передаются в Вордсинк с помощью [**ивордсинк::P уталтворд**](iwordsink-putaltword.md).</span><span class="sxs-lookup"><span data-stu-id="0f284-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="0f284-129">Также рекомендуется, чтобы слова в *пвЦинбуф* соответствовали исходному тексту как можно точнее.</span><span class="sxs-lookup"><span data-stu-id="0f284-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="0f284-130">Например, оставьте прописные и диакритические знаки, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="0f284-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="0f284-131">Этот вызов должен выполняться для каждого слова, полученного от *птекстсаурце* , за исключением тех, для которых был произведен вызов [**Ивордсинк::P уталтворд**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="0f284-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="0f284-132">При сохранении в Вордсинк слово завершается символом ЕОВ.</span><span class="sxs-lookup"><span data-stu-id="0f284-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f284-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0f284-133">Requirements</span></span>



| <span data-ttu-id="0f284-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0f284-134">Requirement</span></span> | <span data-ttu-id="0f284-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0f284-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f284-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f284-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0f284-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f284-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f284-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f284-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0f284-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f284-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f284-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f284-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f284-141"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f284-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f284-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f284-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f284-143">**ивордсинк**</span><span class="sxs-lookup"><span data-stu-id="0f284-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
