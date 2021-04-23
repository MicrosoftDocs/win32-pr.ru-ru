---
description: 'Проверять орфографию в тексте поставщика более тщательно, чем Испеллчеккпровидер:: Check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Метод Икомпрехенсивеспеллчеккпровидер:: Компрехенсивечекк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684615"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="fc55f-103">Метод Икомпрехенсивеспеллчеккпровидер:: Компрехенсивечекк</span><span class="sxs-lookup"><span data-stu-id="fc55f-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="fc55f-104">Проверять орфографию в тексте поставщика более тщательно, чем [**испеллчеккпровидер:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="fc55f-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc55f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc55f-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="fc55f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc55f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc55f-107">*текстовая надпись* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc55f-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc55f-108">Проверяемый текст.</span><span class="sxs-lookup"><span data-stu-id="fc55f-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="fc55f-109">*результат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc55f-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc55f-110">Результат проверки этого текста в виде перечисления орфографических ошибок ([**иенумспеллинжеррор**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="fc55f-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc55f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc55f-111">Return value</span></span>

<span data-ttu-id="fc55f-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="fc55f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="fc55f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc55f-113">Return value</span></span>                                                                             | <span data-ttu-id="fc55f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fc55f-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="fc55f-115"><dt>\_ОК</dt></span><span class="sxs-lookup"><span data-stu-id="fc55f-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="fc55f-116">Удалось.</span><span class="sxs-lookup"><span data-stu-id="fc55f-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="fc55f-117"><dt>E \_ INVALIDARG</dt></span><span class="sxs-lookup"><span data-stu-id="fc55f-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="fc55f-118">*текст* представляет собой пустую строку.</span><span class="sxs-lookup"><span data-stu-id="fc55f-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="fc55f-119"><dt>\_указатель E</dt></span><span class="sxs-lookup"><span data-stu-id="fc55f-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="fc55f-120">*текст* является пустым указателем.</span><span class="sxs-lookup"><span data-stu-id="fc55f-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="fc55f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc55f-121">Remarks</span></span>

<span data-ttu-id="fc55f-122">Этот интерфейс не обязательно должен быть реализован поставщиком проверки орфографии.</span><span class="sxs-lookup"><span data-stu-id="fc55f-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="fc55f-123">Но если поставщик поддерживает два режима проверки орфографии (более быстрый и медленный, но более тщательный), он должен реализовать этот интерфейс в том же объекте, который реализует [**испеллчеккпровидер**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) для поддержки более тщательного режима проверки.</span><span class="sxs-lookup"><span data-stu-id="fc55f-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="fc55f-124">Когда клиент вызывает [**испеллчеккер:: компрехенсивечекк**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), функция проверки орфографии [**будет**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) возвращать поставщик для [**Икомпрехенсивеспеллчеккпровидер**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)и вызывать **икомпрехенсивеспеллчеккпровидер. ComprehensiveCheck** , если интерфейс поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc55f-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="fc55f-125">Если интерфейс не поддерживается, он будет автоматически возвращаться к [**испеллчеккпровидер:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="fc55f-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc55f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc55f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc55f-127">**икомпрехенсивеспеллчеккпровидер**</span><span class="sxs-lookup"><span data-stu-id="fc55f-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="fc55f-128">**иенумспеллинжеррор**</span><span class="sxs-lookup"><span data-stu-id="fc55f-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="fc55f-129">**Испеллчеккер:: Компрехенсивечекк**</span><span class="sxs-lookup"><span data-stu-id="fc55f-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="fc55f-130">**испеллчеккпровидер**</span><span class="sxs-lookup"><span data-stu-id="fc55f-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="fc55f-131">**Испеллчеккпровидер:: Check**</span><span class="sxs-lookup"><span data-stu-id="fc55f-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
