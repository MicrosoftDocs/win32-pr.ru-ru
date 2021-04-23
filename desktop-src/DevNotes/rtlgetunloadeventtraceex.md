---
description: Возвращает размер и расположение динамически выгруженного списка модулей для текущего процесса.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Функция Ртлжетунлоадевенттрацеекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669031"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="7779b-103">Функция Ртлжетунлоадевенттрацеекс</span><span class="sxs-lookup"><span data-stu-id="7779b-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="7779b-104">Возвращает размер и расположение динамически выгруженного списка модулей для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="7779b-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="7779b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7779b-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="7779b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7779b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7779b-107">*ElementSize* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7779b-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7779b-108">Указатель на переменную, которая содержит размер элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="7779b-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="7779b-109">*ElementCount* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7779b-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7779b-110">Указатель на переменную, которая содержит число элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="7779b-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="7779b-111">*Евенттраце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7779b-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7779b-112">Указатель на массив структур **\_ \_ \_ трассировки событий "справа налево" выгрузки** .</span><span class="sxs-lookup"><span data-stu-id="7779b-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="7779b-113">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="7779b-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7779b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7779b-114">Return value</span></span>

<span data-ttu-id="7779b-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7779b-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7779b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7779b-116">Remarks</span></span>

<span data-ttu-id="7779b-117">Загрузчик хранит выгруженные сведения о событиях в расположениях, которые могут быть прочитаны между процессами, используя преимущества того факта, что Ntdll.dll загружается по одному и тому же базовому адресу во всех процессах.</span><span class="sxs-lookup"><span data-stu-id="7779b-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="7779b-118">Если отладчику требуется запросить выгруженную информацию о модулях, он вызывает эту функцию для определения адреса, в котором находятся переменные, а затем запрашивает виртуальную память в целевом процессе по этим адресам для чтения фактических значений.</span><span class="sxs-lookup"><span data-stu-id="7779b-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="7779b-119">Каждый элемент в списке определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7779b-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="7779b-120">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="7779b-120">This function has no associated header file.</span></span> <span data-ttu-id="7779b-121">Связанная библиотека импорта, NTDLL. lib, доступна в комплекте драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="7779b-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="7779b-122">Эту функцию также можно вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7779b-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7779b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7779b-123">Requirements</span></span>



| <span data-ttu-id="7779b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7779b-124">Requirement</span></span> | <span data-ttu-id="7779b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7779b-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7779b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7779b-126">DLL</span></span><br/> | <dl> <span data-ttu-id="7779b-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7779b-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
