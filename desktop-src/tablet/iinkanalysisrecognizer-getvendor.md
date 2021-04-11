---
description: Возвращает имя поставщика Иинканалисисрекогнизер.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: Метод Иинканалисисрекогнизер::-Vendor (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145487"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="30566-103">Метод Иинканалисисрекогнизер:: Vendor</span><span class="sxs-lookup"><span data-stu-id="30566-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="30566-104">Возвращает имя поставщика [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="30566-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30566-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30566-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="30566-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30566-107">*пбстрвендор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="30566-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30566-108">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="30566-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30566-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30566-109">Return value</span></span>

<span data-ttu-id="30566-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="30566-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30566-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30566-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="30566-112">Чтобы избежать утечки памяти, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для \* *пбстрвендор* , когда больше не нужно использовать строку.</span><span class="sxs-lookup"><span data-stu-id="30566-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30566-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30566-113">Requirements</span></span>



| <span data-ttu-id="30566-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30566-114">Requirement</span></span> | <span data-ttu-id="30566-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30566-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30566-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30566-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30566-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="30566-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30566-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30566-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30566-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30566-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="30566-120">Header</span><span class="sxs-lookup"><span data-stu-id="30566-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="30566-121"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30566-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30566-122">DLL</span><span class="sxs-lookup"><span data-stu-id="30566-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30566-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30566-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="30566-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30566-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30566-125">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="30566-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="30566-126">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="30566-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

