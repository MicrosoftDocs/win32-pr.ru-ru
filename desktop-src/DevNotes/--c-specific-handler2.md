---
description: Вызывается компилятором для реализации расширений структурированной обработки исключений.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Функция __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657135"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="683fc-103">\_\_\_Конкретная \_ функция обработчика C</span><span class="sxs-lookup"><span data-stu-id="683fc-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="683fc-104">Вызывается компилятором для реализации расширений структурированной обработки исключений.</span><span class="sxs-lookup"><span data-stu-id="683fc-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="683fc-105">Относительный адрес обработчика, относящегося к конкретному языку, содержится в \_ сведениях очистки, если заданы флаги УНВ \_ \_ ехандлер или УНВ \_ Flag \_ ухандлер.</span><span class="sxs-lookup"><span data-stu-id="683fc-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="683fc-106">Обработчик конкретного языка вызывается как часть поиска обработчика исключений или в процессе очистки.</span><span class="sxs-lookup"><span data-stu-id="683fc-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="683fc-107">Дополнительные сведения см. в разделе [обработчик конкретного языка](/cpp/build/language-specific-handler).</span><span class="sxs-lookup"><span data-stu-id="683fc-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="683fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="683fc-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="683fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="683fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683fc-110">*Ексцептионрекорд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="683fc-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683fc-111">Предоставляет указатель на запись исключения, имеющую стандартное определение Win64.</span><span class="sxs-lookup"><span data-stu-id="683fc-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="683fc-112">*Естаблишерфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="683fc-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683fc-113">Адрес основания фиксированного выделения стека для этой функции.</span><span class="sxs-lookup"><span data-stu-id="683fc-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="683fc-114">*Контекстрекорд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="683fc-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="683fc-115">Указывает на контекст исключения на момент возникновения исключения (в случае обработчика исключений) или текущего контекста очистки (в случае обработчика завершения).</span><span class="sxs-lookup"><span data-stu-id="683fc-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="683fc-116">*Диспатчерконтекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="683fc-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="683fc-117">Указывает на контекст Dispatcher для этой функции.</span><span class="sxs-lookup"><span data-stu-id="683fc-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="683fc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="683fc-118">Requirements</span></span>



| <span data-ttu-id="683fc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="683fc-119">Requirement</span></span> | <span data-ttu-id="683fc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="683fc-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="683fc-121">Header</span><span class="sxs-lookup"><span data-stu-id="683fc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="683fc-122"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="683fc-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="683fc-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="683fc-123">Library</span></span><br/> | <dl> <span data-ttu-id="683fc-124"><dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="683fc-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="683fc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="683fc-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="683fc-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="683fc-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

