---
title: " Директива Error"
description: Директива препроцессора, которая создает сообщения об ошибках во время компиляции.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- HLSL директива Error
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411794"
---
# <a name="error-directive"></a><span data-ttu-id="5cdff-104">\#Директива Error</span><span class="sxs-lookup"><span data-stu-id="5cdff-104">\#error Directive</span></span>

<span data-ttu-id="5cdff-105">Директива препроцессора, которая создает сообщения об ошибках во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="5cdff-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="5cdff-106">\#*маркер ошибки — строка*</span><span class="sxs-lookup"><span data-stu-id="5cdff-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5cdff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cdff-107">Parameters</span></span>



| <span data-ttu-id="5cdff-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5cdff-108">Item</span></span>                                                                                    | <span data-ttu-id="5cdff-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5cdff-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cdff-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Строка токена*</span><span class="sxs-lookup"><span data-stu-id="5cdff-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="5cdff-111">Сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5cdff-111">Error message.</span></span> <span data-ttu-id="5cdff-112">Этот параметр состоит из ряда токенов, таких как ключевые слова, константы или полные инструкции.</span><span class="sxs-lookup"><span data-stu-id="5cdff-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="5cdff-113">Строка токена подлежит раскрытию макросов.</span><span class="sxs-lookup"><span data-stu-id="5cdff-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5cdff-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5cdff-114">Remarks</span></span>

<span data-ttu-id="5cdff-115">\#директивы Error наиболее полезны для обнаружения несоответствий в программировании и нарушения ограничений во время предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="5cdff-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="5cdff-116">При \# обнаружении директивы ошибки компиляция завершается.</span><span class="sxs-lookup"><span data-stu-id="5cdff-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="5cdff-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="5cdff-117">Examples</span></span>

<span data-ttu-id="5cdff-118">В следующем примере демонстрируется обработка ошибок во время предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="5cdff-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="5cdff-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cdff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cdff-120">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5cdff-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





