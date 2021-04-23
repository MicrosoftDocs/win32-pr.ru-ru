---
description: Умножает расширенные целые числа.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Функция Ртлекстендединтежермултипли
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665439"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="76c24-103">Функция Ртлекстендединтежермултипли</span><span class="sxs-lookup"><span data-stu-id="76c24-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="76c24-104">\[Функция **ртлекстендединтежермултипли** экспортируется для поддержки существующих двоичных файлов драйверов и является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="76c24-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="76c24-105">Для повышения производительности используйте поддержку компилятора для 64-разрядных целочисленных операций.\]</span><span class="sxs-lookup"><span data-stu-id="76c24-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="76c24-106">Умножает расширенные целые числа.</span><span class="sxs-lookup"><span data-stu-id="76c24-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c24-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76c24-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="76c24-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76c24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76c24-109">*Множимое* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76c24-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c24-110">Множимое.</span><span class="sxs-lookup"><span data-stu-id="76c24-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="76c24-111">*Множитель* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76c24-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c24-112">Множитель.</span><span class="sxs-lookup"><span data-stu-id="76c24-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76c24-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76c24-113">Return value</span></span>

<span data-ttu-id="76c24-114">Возвращает результат умножения.</span><span class="sxs-lookup"><span data-stu-id="76c24-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="76c24-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76c24-115">Remarks</span></span>

<span data-ttu-id="76c24-116">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="76c24-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c24-117">Требования</span><span class="sxs-lookup"><span data-stu-id="76c24-117">Requirements</span></span>



| <span data-ttu-id="76c24-118">Требование</span><span class="sxs-lookup"><span data-stu-id="76c24-118">Requirement</span></span> | <span data-ttu-id="76c24-119">Значение</span><span class="sxs-lookup"><span data-stu-id="76c24-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76c24-120">DLL</span><span class="sxs-lookup"><span data-stu-id="76c24-120">DLL</span></span><br/> | <dl> <span data-ttu-id="76c24-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76c24-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
