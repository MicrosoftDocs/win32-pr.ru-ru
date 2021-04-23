---
description: Указывает, получена ли указанная распознанная строка из системного словаря, пользовательского словаря или списка слов.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Метод Иконтекстноде:: Исалтернатестрингсуппортед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662407"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="bbf6f-103">Метод Иконтекстноде:: Исалтернатестрингсуппортед</span><span class="sxs-lookup"><span data-stu-id="bbf6f-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="bbf6f-104">Указывает, получена ли указанная распознанная строка из системного словаря, пользовательского словаря или списка слов.</span><span class="sxs-lookup"><span data-stu-id="bbf6f-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="bbf6f-105">Для определения того, поддерживается ли строка, можно использовать любые ограниченные данные, такие как списков слов, направляющих или фактоидс, в любом соответствующем узле подсказок.</span><span class="sxs-lookup"><span data-stu-id="bbf6f-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf6f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbf6f-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="bbf6f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbf6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf6f-108">*бстралтернатестринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbf6f-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf6f-109">Распознанная строка для проверки.</span><span class="sxs-lookup"><span data-stu-id="bbf6f-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="bbf6f-110">*пфиссуппортед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bbf6f-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbf6f-111">**Вариант \_ Значение TRUE** , если указанная строка поддерживается [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) с любыми соответствующими узлами подсказок; **Вариант \_ Значение FALSE** , если не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bbf6f-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf6f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbf6f-112">Return value</span></span>

<span data-ttu-id="bbf6f-113">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bbf6f-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf6f-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="bbf6f-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf6f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bbf6f-115">Requirements</span></span>



| <span data-ttu-id="bbf6f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bbf6f-116">Requirement</span></span> | <span data-ttu-id="bbf6f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bbf6f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf6f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbf6f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf6f-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bbf6f-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bbf6f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbf6f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf6f-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bbf6f-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bbf6f-122">Header</span><span class="sxs-lookup"><span data-stu-id="bbf6f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf6f-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bbf6f-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bbf6f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bbf6f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbf6f-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbf6f-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bbf6f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbf6f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf6f-127">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="bbf6f-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




