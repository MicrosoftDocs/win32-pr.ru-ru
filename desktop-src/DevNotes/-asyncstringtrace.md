---
description: Функция Асинкстрингтраце — завершает настройку буфера трассировки с необязательными полями для трассировок в стиле sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Функция Асинкстрингтраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085802"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="3c0e3-103">Функция Асинкстрингтраце</span><span class="sxs-lookup"><span data-stu-id="3c0e3-103">AsyncStringTrace function</span></span>

<span data-ttu-id="3c0e3-104">Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c0e3-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="3c0e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c0e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0e3-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c0e3-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0e3-108">32-разрядный параметр трассировки, используемый для фильтрации на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="3c0e3-109">*сзформат*</span><span class="sxs-lookup"><span data-stu-id="3c0e3-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0e3-110">Строка, завершающаяся нулем, которая описывает формат трассировки.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="3c0e3-111">*Фломастер*</span><span class="sxs-lookup"><span data-stu-id="3c0e3-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0e3-112">Маркер для функций **vsprintf** .</span><span class="sxs-lookup"><span data-stu-id="3c0e3-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0e3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c0e3-113">Return value</span></span>

<span data-ttu-id="3c0e3-114">Эта функция возвращает длину инструкции трассировки в байтах.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0e3-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c0e3-115">Remarks</span></span>

<span data-ttu-id="3c0e3-116">Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="3c0e3-117">Тип данных « **\_ список ва** » — это стандартный тип, который используется для хранения информации, необходимой для **\_ завершения** макросов «# **\_ arg** » и «ва».</span><span class="sxs-lookup"><span data-stu-id="3c0e3-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="3c0e3-118">Дополнительные сведения см. в разделе [стандартные типы](/cpp/c-runtime-library/standard-types?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="3c0e3-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="3c0e3-119">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3c0e3-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0e3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3c0e3-120">Requirements</span></span>



| <span data-ttu-id="3c0e3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3c0e3-121">Requirement</span></span> | <span data-ttu-id="3c0e3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3c0e3-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0e3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3c0e3-123">DLL</span></span><br/> | <dl> <span data-ttu-id="3c0e3-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c0e3-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

