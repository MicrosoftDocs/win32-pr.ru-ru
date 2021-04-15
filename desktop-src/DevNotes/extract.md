---
description: Функция Extract извлекает файлы из CAB-файла.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Извлечение функции
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648863"
---
# <a name="extract-function"></a><span data-ttu-id="e6abb-103">Извлечение функции</span><span class="sxs-lookup"><span data-stu-id="e6abb-103">Extract function</span></span>

<span data-ttu-id="e6abb-104">\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.\]</span><span class="sxs-lookup"><span data-stu-id="e6abb-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="e6abb-105">Функция **Extract** извлекает файлы из CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="e6abb-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6abb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6abb-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="e6abb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6abb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6abb-108">*ps*</span><span class="sxs-lookup"><span data-stu-id="e6abb-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="e6abb-109">Указатель на структуру [**сеанса**](session.md) , содержащую сведения о текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="e6abb-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="e6abb-110">*лпкабнаме*</span><span class="sxs-lookup"><span data-stu-id="e6abb-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="e6abb-111">Указатель на имя CAB-файла, из которого должны быть извлечены файлы.</span><span class="sxs-lookup"><span data-stu-id="e6abb-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6abb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6abb-112">Return value</span></span>

<span data-ttu-id="e6abb-113">Если функция завершается успешно, возвращается значение **\_ ОК**; в противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e6abb-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6abb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6abb-114">Remarks</span></span>

<span data-ttu-id="e6abb-115">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e6abb-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6abb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e6abb-116">Requirements</span></span>



| <span data-ttu-id="e6abb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e6abb-117">Requirement</span></span> | <span data-ttu-id="e6abb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e6abb-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6abb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e6abb-119">DLL</span></span><br/> | <dl> <span data-ttu-id="e6abb-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6abb-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6abb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6abb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6abb-122">**делетикстрактедфилес**</span><span class="sxs-lookup"><span data-stu-id="e6abb-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="e6abb-123">**ИНТЕГРИРОВАН**</span><span class="sxs-lookup"><span data-stu-id="e6abb-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="e6abb-124">**СЕССИИ**</span><span class="sxs-lookup"><span data-stu-id="e6abb-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
