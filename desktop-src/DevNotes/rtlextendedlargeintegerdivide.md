---
description: Делит расширенные целые числа.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: Функция Ртлекстендедларжеинтежердивиде
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668942"
---
# <a name="rtlextendedlargeintegerdivide-function"></a><span data-ttu-id="ad9f9-103">Функция Ртлекстендедларжеинтежердивиде</span><span class="sxs-lookup"><span data-stu-id="ad9f9-103">RtlExtendedLargeIntegerDivide function</span></span>

<span data-ttu-id="ad9f9-104">\[Функция **ртлекстендедларжеинтежердивиде** экспортируется для поддержки существующих двоичных файлов драйверов и является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-104">\[The **RtlExtendedLargeIntegerDivide** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="ad9f9-105">Для повышения производительности используйте поддержку компилятора для 64-разрядных целочисленных операций.\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="ad9f9-106">Делит расширенные целые числа.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-106">Divides extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad9f9-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a><span data-ttu-id="ad9f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad9f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9f9-109">*Делимое* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-109">*Dividend* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-110">Дивиденд.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-110">Dividend.</span></span>

</dd> <dt>

<span data-ttu-id="ad9f9-111">*Делитель* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-111">*Divisor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-112">Равн.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="ad9f9-113">*Остаток от деления* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-113">*Remainder* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-114">Указатель на остаток от деления.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-114">Pointer to division remainder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9f9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad9f9-115">Return value</span></span>

<span data-ttu-id="ad9f9-116">Возвращает результат операции деления.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-116">Returns the result of the division operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9f9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad9f9-117">Remarks</span></span>

<span data-ttu-id="ad9f9-118">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ad9f9-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9f9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ad9f9-119">Requirements</span></span>



| <span data-ttu-id="ad9f9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ad9f9-120">Requirement</span></span> | <span data-ttu-id="ad9f9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ad9f9-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9f9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ad9f9-122">DLL</span></span><br/> | <dl> <span data-ttu-id="ad9f9-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad9f9-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
