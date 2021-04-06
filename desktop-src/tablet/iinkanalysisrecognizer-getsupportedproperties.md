---
description: Получает глобальные уникальные идентификаторы (GUID) для свойств, которые эта Иинканалисисрекогнизер может создать для результатов анализа.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Метод Иинканалисисрекогнизер:: Жетсуппортедпропертиес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991159"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="156dc-103">Метод Иинканалисисрекогнизер:: Жетсуппортедпропертиес</span><span class="sxs-lookup"><span data-stu-id="156dc-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="156dc-104">Получает глобальные уникальные идентификаторы (GUID) для свойств, которые эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) может создать для результатов анализа.</span><span class="sxs-lookup"><span data-stu-id="156dc-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="156dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="156dc-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="156dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="156dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156dc-107">*пулпропертиескаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="156dc-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="156dc-108">Число идентификаторов GUID в *пппропертиес*.</span><span class="sxs-lookup"><span data-stu-id="156dc-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="156dc-109">*пппропертиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="156dc-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="156dc-110">Указатель на идентификаторы GUID свойств, которые эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) может создать для результатов анализа.</span><span class="sxs-lookup"><span data-stu-id="156dc-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="156dc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="156dc-111">Return value</span></span>

<span data-ttu-id="156dc-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="156dc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="156dc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="156dc-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="156dc-114">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пппропертиес* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="156dc-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="156dc-115">Распознаватель может поддерживать линии метрик, Номера строк, уровни достоверности и т. д.</span><span class="sxs-lookup"><span data-stu-id="156dc-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="156dc-116">Полный список свойств, которые может поддерживать распознаватель, см. в разделе [константы рекогнитионпроперти](recognitionproperty-constants.md).</span><span class="sxs-lookup"><span data-stu-id="156dc-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="156dc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="156dc-117">Requirements</span></span>



| <span data-ttu-id="156dc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="156dc-118">Requirement</span></span> | <span data-ttu-id="156dc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="156dc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="156dc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="156dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="156dc-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="156dc-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="156dc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="156dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="156dc-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="156dc-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="156dc-124">Header</span><span class="sxs-lookup"><span data-stu-id="156dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="156dc-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="156dc-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="156dc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="156dc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="156dc-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="156dc-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="156dc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="156dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="156dc-129">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="156dc-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="156dc-130">Константы Рекогнитионпроперти</span><span class="sxs-lookup"><span data-stu-id="156dc-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="156dc-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="156dc-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

