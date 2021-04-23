---
description: Функция Делетикстрактедфилес удаляет файлы, извлеченные функцией Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Функция Делетикстрактедфилес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657215"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="9b4ab-103">Функция Делетикстрактедфилес</span><span class="sxs-lookup"><span data-stu-id="9b4ab-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="9b4ab-104">\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется.\]</span><span class="sxs-lookup"><span data-stu-id="9b4ab-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="9b4ab-105">Функция **делетикстрактедфилес** удаляет файлы, извлеченные функцией [**Extract**](extract.md) .</span><span class="sxs-lookup"><span data-stu-id="9b4ab-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b4ab-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="9b4ab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b4ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4ab-108">*ps*</span><span class="sxs-lookup"><span data-stu-id="9b4ab-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4ab-109">Указатель на структуру [**сеанса**](session.md) , содержащую сведения о текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="9b4ab-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="9b4ab-110">Эта функция освобождает память в элементе **пфилелист** этой структуры и задает для **пфилелист** **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b4ab-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b4ab-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b4ab-111">Return value</span></span>

<span data-ttu-id="9b4ab-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9b4ab-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b4ab-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b4ab-113">Remarks</span></span>

<span data-ttu-id="9b4ab-114">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9b4ab-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b4ab-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9b4ab-115">Requirements</span></span>



| <span data-ttu-id="9b4ab-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9b4ab-116">Requirement</span></span> | <span data-ttu-id="9b4ab-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9b4ab-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4ab-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9b4ab-118">DLL</span></span><br/> | <dl> <span data-ttu-id="9b4ab-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b4ab-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4ab-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b4ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4ab-121">**Распаковк**</span><span class="sxs-lookup"><span data-stu-id="9b4ab-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="9b4ab-122">**СЕССИИ**</span><span class="sxs-lookup"><span data-stu-id="9b4ab-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
