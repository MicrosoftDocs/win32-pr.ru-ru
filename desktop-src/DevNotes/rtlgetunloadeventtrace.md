---
description: Позволяет коду дампа получать выгруженные сведения о модуле из Ntdll.dll для хранения в минидампа.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Функция Ртлжетунлоадевенттраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648913"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="f0ae3-103">Функция Ртлжетунлоадевенттраце</span><span class="sxs-lookup"><span data-stu-id="f0ae3-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="f0ae3-104">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="f0ae3-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="f0ae3-105">Позволяет коду дампа получать выгруженные сведения о модуле из Ntdll.dll для хранения в минидампа.</span><span class="sxs-lookup"><span data-stu-id="f0ae3-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ae3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0ae3-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="f0ae3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0ae3-107">Parameters</span></span>

<span data-ttu-id="f0ae3-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="f0ae3-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0ae3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0ae3-109">Return value</span></span>

<span data-ttu-id="f0ae3-110">Эта функция возвращает указатель на массив.</span><span class="sxs-lookup"><span data-stu-id="f0ae3-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="f0ae3-111">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f0ae3-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ae3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0ae3-112">Remarks</span></span>

<span data-ttu-id="f0ae3-113">Массив Ртлпунлоадевенттраце определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f0ae3-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="f0ae3-114">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="f0ae3-114">This function has no associated header file.</span></span> <span data-ttu-id="f0ae3-115">Связанная библиотека импорта, NTDLL. lib, доступна в комплекте драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="f0ae3-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="f0ae3-116">Эту функцию также можно вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f0ae3-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ae3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f0ae3-117">Requirements</span></span>



| <span data-ttu-id="f0ae3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f0ae3-118">Requirement</span></span> | <span data-ttu-id="f0ae3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f0ae3-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ae3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ae3-120">DLL</span></span><br/> | <dl> <span data-ttu-id="f0ae3-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ae3-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
