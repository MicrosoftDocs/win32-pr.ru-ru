---
title: Функция RoFailFastWithErrorContextInternal2
description: Вызывает исключение, которое не является непрерывным в текущем процессе, а также позволяет включить дополнительный контекст ошибки, еще не записанный операционной системой.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105719160"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="5b024-103">Функция RoFailFastWithErrorContextInternal2</span><span class="sxs-lookup"><span data-stu-id="5b024-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="5b024-104">Вызывает исключение, которое не является непрерывным в текущем процессе, а также позволяет включить дополнительный контекст ошибки, который еще не был захвачен операционной системой (ОС).</span><span class="sxs-lookup"><span data-stu-id="5b024-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b024-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b024-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="5b024-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b024-106">Parameters</span></span>

`hrError`

<span data-ttu-id="5b024-107">Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="5b024-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="5b024-108">Значение **HRESULT** , связанное с текущей ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5b024-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="5b024-109">Исключение вызывается для любого значения *хреррор*.</span><span class="sxs-lookup"><span data-stu-id="5b024-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="5b024-110">Тип: **[ulong](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b024-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b024-111">Число элементов в массиве *астоведексцептионпоинтерс* .</span><span class="sxs-lookup"><span data-stu-id="5b024-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="5b024-112">Тип: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="5b024-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="5b024-113">Массив указателей на [**STOWED_EXCEPTION_INFORMATION_V2ные**](../../wer/stowed-exception-information-v2.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="5b024-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="5b024-114">Каждая структура содержит сведения, описывающие исключение заполнения.</span><span class="sxs-lookup"><span data-stu-id="5b024-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="5b024-115">Сведения в этих структурах затем отправляются в отчеты об ошибках Windows (WER) вместе со сведениями об исключении заполнения, которые были перехвачены платформой.</span><span class="sxs-lookup"><span data-stu-id="5b024-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b024-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b024-116">Return value</span></span>

<span data-ttu-id="5b024-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5b024-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b024-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b024-118">Remarks</span></span>

<span data-ttu-id="5b024-119">**RoFailFastWithErrorContextInternal2** не связан с библиотекой импорта или файлом заголовка.</span><span class="sxs-lookup"><span data-stu-id="5b024-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="5b024-120">Его можно вызвать, сначала используя функцию [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (для загрузки `ComBase.dll` ), а затем вызвав функцию [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса **RoFailFastWithErrorContextInternal2**.</span><span class="sxs-lookup"><span data-stu-id="5b024-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="5b024-121">Дополнительные сведения см. в разделе [функция рофаилфаствисеррорконтекст](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span><span class="sxs-lookup"><span data-stu-id="5b024-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b024-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5b024-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5b024-123">**Целевая платформа**</span><span class="sxs-lookup"><span data-stu-id="5b024-123">**Target Platform**</span></span> | <span data-ttu-id="5b024-124">Windows</span><span class="sxs-lookup"><span data-stu-id="5b024-124">Windows</span></span> |
| <span data-ttu-id="5b024-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="5b024-125">**Header**</span></span> | <span data-ttu-id="5b024-126">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5b024-126">N/A</span></span> |
| <span data-ttu-id="5b024-127">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="5b024-127">**Library**</span></span> | <span data-ttu-id="5b024-128">Н/Д</span><span class="sxs-lookup"><span data-stu-id="5b024-128">N/A</span></span> |
| <span data-ttu-id="5b024-129">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="5b024-129">**DLL**</span></span> | <span data-ttu-id="5b024-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="5b024-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="5b024-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b024-131">See also</span></span>

* [<span data-ttu-id="5b024-132">Функция Рофаилфаствисеррорконтекст</span><span class="sxs-lookup"><span data-stu-id="5b024-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)