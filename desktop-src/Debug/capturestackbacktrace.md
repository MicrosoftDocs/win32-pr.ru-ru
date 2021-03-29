---
UID: ''
title: Функция Каптурестаккбакктраце
description: Захватывает обратную трассировку стека, выполнив проход вверх по стеку.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "105654261"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="652d9-103">Функция Каптурестаккбакктраце</span><span class="sxs-lookup"><span data-stu-id="652d9-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="652d9-104">Описание</span><span class="sxs-lookup"><span data-stu-id="652d9-104">Description</span></span>

<span data-ttu-id="652d9-105">Фиксирует обратную трассировку стека, выполнив проход вверх по стеку и записывая сведения для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="652d9-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="652d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="652d9-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="652d9-107">Фраместоскип [in]</span><span class="sxs-lookup"><span data-stu-id="652d9-107">FramesToSkip [in]</span></span>

<span data-ttu-id="652d9-108">Число кадров, которые нужно пропустить с начала обратной трассировки.</span><span class="sxs-lookup"><span data-stu-id="652d9-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="652d9-109">Фраместокаптуре [in]</span><span class="sxs-lookup"><span data-stu-id="652d9-109">FramesToCapture [in]</span></span>

<span data-ttu-id="652d9-110">Число кадров для записи.</span><span class="sxs-lookup"><span data-stu-id="652d9-110">The number of frames to be captured.</span></span>
<span data-ttu-id="652d9-111">Вы можете захватить до **максушорт** кадров.</span><span class="sxs-lookup"><span data-stu-id="652d9-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="652d9-112">**Windows Server 2003 и Windows XP:**  Сумма параметров *фраместоскип* и *фраместокаптуре* должна быть меньше 63.</span><span class="sxs-lookup"><span data-stu-id="652d9-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="652d9-113">Невыполненная трассировка [out]</span><span class="sxs-lookup"><span data-stu-id="652d9-113">BackTrace [out]</span></span>

<span data-ttu-id="652d9-114">Массив указателей, захваченных из текущей трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="652d9-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="652d9-115">Бакктрацехаш [out, необязательно]</span><span class="sxs-lookup"><span data-stu-id="652d9-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="652d9-116">Значение, которое может быть использовано для Организации хэш-таблиц.</span><span class="sxs-lookup"><span data-stu-id="652d9-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="652d9-117">Если этот параметр имеет **значение NULL**, хэш-значение не вычислено.</span><span class="sxs-lookup"><span data-stu-id="652d9-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="652d9-118">Это значение вычисляется на основе значений указателей, возвращаемых в массиве отслеживаний.</span><span class="sxs-lookup"><span data-stu-id="652d9-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="652d9-119">Две идентичные трассировки стека будут формировать идентичные хэш-значения.</span><span class="sxs-lookup"><span data-stu-id="652d9-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="652d9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="652d9-120">Returns</span></span>

<span data-ttu-id="652d9-121">Число захваченных кадров.</span><span class="sxs-lookup"><span data-stu-id="652d9-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="652d9-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="652d9-122">Remarks</span></span>

<span data-ttu-id="652d9-123">Функция **каптурестаккбакктраце** определяется как функция **ртлкаптурестаккбакктраце** (определение включается в Windows SDK, начиная с Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="652d9-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="652d9-124">Дополнительные сведения см. в разделе Винбасе. h и WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="652d9-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="652d9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="652d9-125">See also</span></span>
