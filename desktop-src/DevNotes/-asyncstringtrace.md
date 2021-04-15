---
description: Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле sprintf.
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
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648107"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="711e7-103">Функция Асинкстрингтраце</span><span class="sxs-lookup"><span data-stu-id="711e7-103">AsyncStringTrace function</span></span>

<span data-ttu-id="711e7-104">Завершает настройку буфера трассировки с необязательными полями для трассировок в стиле **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="711e7-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="711e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="711e7-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="711e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="711e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711e7-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="711e7-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711e7-108">32-разрядный параметр трассировки, используемый для фильтрации на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="711e7-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="711e7-109">*сзформат*</span><span class="sxs-lookup"><span data-stu-id="711e7-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="711e7-110">Строка, завершающаяся нулем, которая описывает формат трассировки.</span><span class="sxs-lookup"><span data-stu-id="711e7-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="711e7-111">*Фломастер*</span><span class="sxs-lookup"><span data-stu-id="711e7-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="711e7-112">Маркер для функций **vsprintf** .</span><span class="sxs-lookup"><span data-stu-id="711e7-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="711e7-113">Return value</span></span>

<span data-ttu-id="711e7-114">Эта функция возвращает длину инструкции трассировки в байтах.</span><span class="sxs-lookup"><span data-stu-id="711e7-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="711e7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="711e7-115">Remarks</span></span>

<span data-ttu-id="711e7-116">Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.</span><span class="sxs-lookup"><span data-stu-id="711e7-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="711e7-117">Тип данных « **\_ список ва** » — это стандартный тип, который используется для хранения информации, необходимой для **\_ завершения** макросов «# **\_ arg** » и «ва».</span><span class="sxs-lookup"><span data-stu-id="711e7-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="711e7-118">Дополнительные сведения см. в разделе [стандартные типы](/cpp/c-runtime-library/standard-types?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="711e7-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="711e7-119">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="711e7-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="711e7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="711e7-120">Requirements</span></span>



| <span data-ttu-id="711e7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="711e7-121">Requirement</span></span> | <span data-ttu-id="711e7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="711e7-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="711e7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="711e7-123">DLL</span></span><br/> | <dl> <span data-ttu-id="711e7-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711e7-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

