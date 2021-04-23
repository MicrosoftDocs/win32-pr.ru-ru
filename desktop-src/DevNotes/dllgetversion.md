---
description: Функция Дллжетверсион извлекает номер версии Cabinet.dll используя структуру КАБИНЕТДЛЛВЕРСИОНИНФО.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Функция Дллжетверсион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648104"
---
# <a name="dllgetversion-function"></a><span data-ttu-id="c1437-103">Функция Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="c1437-103">DllGetVersion function</span></span>

<span data-ttu-id="c1437-104">\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.\]</span><span class="sxs-lookup"><span data-stu-id="c1437-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="c1437-105">Функция **дллжетверсион** извлекает номер версии Cabinet.dll используя структуру [**кабинетдллверсионинфо**](cabinetdllversioninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c1437-105">The **DllGetVersion** function retrieves the version number of Cabinet.dll using the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1437-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1437-106">Syntax</span></span>


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a><span data-ttu-id="c1437-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1437-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1437-108">*пкдви*</span><span class="sxs-lookup"><span data-stu-id="c1437-108">*pcdvi*</span></span> 
</dt> <dd>

<span data-ttu-id="c1437-109">Указатель на структуру [**кабинетдллверсионинфо**](cabinetdllversioninfo.md) , содержащую сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="c1437-109">Pointer to the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure that contains the version information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1437-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1437-110">Return value</span></span>

<span data-ttu-id="c1437-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c1437-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1437-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1437-112">Remarks</span></span>

<span data-ttu-id="c1437-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c1437-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1437-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c1437-114">Requirements</span></span>



| <span data-ttu-id="c1437-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c1437-115">Requirement</span></span> | <span data-ttu-id="c1437-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c1437-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1437-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c1437-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c1437-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1437-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1437-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1437-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1437-120">**кабинетдллверсионинфо**</span><span class="sxs-lookup"><span data-stu-id="c1437-120">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md)
</dt> <dt>

[<span data-ttu-id="c1437-121">**жетдллверсион**</span><span class="sxs-lookup"><span data-stu-id="c1437-121">**GetDllVersion**</span></span>](getdllversion.md)
</dt> </dl>

 

 
