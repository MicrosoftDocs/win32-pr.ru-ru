---
description: Извлекает сведения о пространстве, используемом кэшем автономные файлы.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Функция Кскжетспацеусажев
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648923"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="d3c2c-103">Функция Кскжетспацеусажев</span><span class="sxs-lookup"><span data-stu-id="d3c2c-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="d3c2c-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="d3c2c-105">Извлекает сведения о пространстве, используемом кэшем автономные файлы.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c2c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3c2c-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="d3c2c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3c2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c2c-108">*лптзлокатион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-109">Расположение каталога кэша.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-110">*двсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-111">Размер буфера *лптзлокатион* в символах.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-112">*лпдвмаксспацехигх* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-113">**Параметр DWORD** высокого порядка для максимального числа байтов, доступных в кэше.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-114">*лпдвмаксспацелов* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-115">**Параметр DWORD** нижнего порядка для максимального числа байтов, доступных в кэше.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-116">*лпдвкуррентспацехигх* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-117">**Параметр DWORD** высокого порядка текущего числа байтов, доступных в кэше.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-118">*лпдвкуррентспацелов* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-119">**Параметр DWORD** нижнего порядка текущего числа байтов, доступных в кэше.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-120">*лпкнттоталфилес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-121">Общее число файлов в кэше.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2c-122">*лпкнттоталдирс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c2c-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c2c-123">Общее число каталогов в кэше.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c2c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3c2c-124">Return value</span></span>

<span data-ttu-id="d3c2c-125">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="d3c2c-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c2c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3c2c-126">Remarks</span></span>

<span data-ttu-id="d3c2c-127">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d3c2c-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c2c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d3c2c-128">Requirements</span></span>



| <span data-ttu-id="d3c2c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d3c2c-129">Requirement</span></span> | <span data-ttu-id="d3c2c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d3c2c-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c2c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c2c-131">DLL</span></span><br/> | <dl> <span data-ttu-id="d3c2c-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c2c-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
