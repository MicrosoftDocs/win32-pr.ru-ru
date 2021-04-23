---
description: Помещает в объект Ивордсинк альтернативное слово и его расположение.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: 'Ивордсинк: метод:P Уталтворд (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692182"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="c0143-103">Ивордсинк: метод:P Уталтворд</span><span class="sxs-lookup"><span data-stu-id="c0143-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="c0143-104">Помещает в объект [**ивордсинк**](iwordsink.md) альтернативное слово и его расположение.</span><span class="sxs-lookup"><span data-stu-id="c0143-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0143-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0143-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="c0143-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0143-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0143-107">*КВК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0143-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0143-108">Число символов в *пвЦинбуф*.</span><span class="sxs-lookup"><span data-stu-id="c0143-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="c0143-109">*пвЦинбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0143-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0143-110">Указатель на буфер, содержащий альтернативную форму слова из исходного текста.</span><span class="sxs-lookup"><span data-stu-id="c0143-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="c0143-111">Этот параметр не изменяется **путалтворд**.</span><span class="sxs-lookup"><span data-stu-id="c0143-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="c0143-112">При необходимости можно передать параметр *птекстсаурце* из [**Ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="c0143-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="c0143-113">*квксрклен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0143-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0143-114">Количество символов в исходном текстовом буфере (обозначенное параметром *птекстсаурце* в [**Ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)), соответствующее слову, содержащемуся в *пвЦинбуф*.</span><span class="sxs-lookup"><span data-stu-id="c0143-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="c0143-115">*квксркпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0143-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0143-116">Начальное расположение слова в *пвЦинбуф* в исходном текстовом буфере (указывается параметром *птекстсаурце* в [**ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="c0143-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0143-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0143-117">Return value</span></span>

<span data-ttu-id="c0143-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c0143-118">This method can return one of these values.</span></span>



| <span data-ttu-id="c0143-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c0143-119">Return code</span></span>                                                                                              | <span data-ttu-id="c0143-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c0143-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0143-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c0143-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="c0143-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="c0143-122">The operation was completed successfully.</span></span> <span data-ttu-id="c0143-123">Также указывает, что больше не осталось никакого текста для обработки.</span><span class="sxs-lookup"><span data-stu-id="c0143-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c0143-124"><dt>**Языковая \_ \_крупное \_ слово S**</dt></span><span class="sxs-lookup"><span data-stu-id="c0143-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="c0143-125">Значение *КВК* больше, чем значение *улмакстокенсизе* , указанное в [**ивордбреакер:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="c0143-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0143-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0143-126">Remarks</span></span>

<span data-ttu-id="c0143-127">**Путалтворд** помещает в [**ивордсинк**](iwordsink.md)альтернативную форму слова.</span><span class="sxs-lookup"><span data-stu-id="c0143-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="c0143-128">Слово помещается в ту же точку, что и исходное слово в источнике текста (*птекстсаурце* в [**Ивордбреакер:: бреактекст**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="c0143-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="c0143-129">По умолчанию **путалтворд** завершает слова с **вордрепм Break \_ \_ Еов** , заданными в перечислимом типе [**вордреп \_ \_ типа Break**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c0143-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0143-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c0143-130">Requirements</span></span>



| <span data-ttu-id="c0143-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c0143-131">Requirement</span></span> | <span data-ttu-id="c0143-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c0143-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0143-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0143-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c0143-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0143-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c0143-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0143-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c0143-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c0143-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0143-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c0143-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0143-138"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0143-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0143-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0143-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0143-140">**ивордсинк**</span><span class="sxs-lookup"><span data-stu-id="c0143-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
