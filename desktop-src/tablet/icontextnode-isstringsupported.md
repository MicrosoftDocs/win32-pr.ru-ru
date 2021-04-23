---
description: Указывает, поступил ли распознанная строка этого Иконтекстноде из системного словаря, пользовательского словаря или списка слов.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Метод Иконтекстноде:: Исстрингсуппортед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692437"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="c4f86-103">Метод Иконтекстноде:: Исстрингсуппортед</span><span class="sxs-lookup"><span data-stu-id="c4f86-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="c4f86-104">Указывает, поступил ли распознанная строка этого [**иконтекстноде**](icontextnode.md) из системного словаря, пользовательского словаря или списка слов.</span><span class="sxs-lookup"><span data-stu-id="c4f86-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4f86-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="c4f86-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4f86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f86-107">*пфиссуппортед* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c4f86-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f86-108">**Вариант \_ Значение TRUE** , если распознанное строковое значение данного [**Иконтекстноде**](icontextnode.md) поддерживается [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) с любыми соответствующими узлами подсказок. в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="c4f86-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f86-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4f86-109">Return value</span></span>

<span data-ttu-id="c4f86-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c4f86-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f86-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c4f86-111">Requirements</span></span>



| <span data-ttu-id="c4f86-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c4f86-112">Requirement</span></span> | <span data-ttu-id="c4f86-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f86-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f86-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4f86-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f86-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c4f86-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c4f86-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4f86-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f86-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4f86-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c4f86-118">Header</span><span class="sxs-lookup"><span data-stu-id="c4f86-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4f86-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c4f86-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c4f86-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c4f86-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4f86-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4f86-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c4f86-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4f86-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f86-123">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="c4f86-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




