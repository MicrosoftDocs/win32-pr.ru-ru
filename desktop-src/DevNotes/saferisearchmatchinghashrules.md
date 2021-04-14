---
description: Возвращает уровень правила идентификации хэша, соответствующего указанному хэшу.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Функция Саферисеарчматчингхашрулес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496488"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="b8582-103">Функция Саферисеарчматчингхашрулес</span><span class="sxs-lookup"><span data-stu-id="b8582-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="b8582-104">Возвращает уровень правила идентификации хэша, соответствующего указанному хэшу.</span><span class="sxs-lookup"><span data-stu-id="b8582-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="b8582-105">Эта функция не имеет связанной библиотеки импорта и не объявлена в общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="b8582-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="b8582-106">Необходимо определить указатель функции с сигнатурой этой функции, и для динамической привязки к Advapi32.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b8582-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="b8582-107">Для вычисления политик ограниченного использования программ рекомендуется использовать функцию [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) .</span><span class="sxs-lookup"><span data-stu-id="b8582-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8582-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8582-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b8582-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8582-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8582-110">*HashAlgorithm* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b8582-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8582-111">Идентификатор алгоритма, используемого для создания хэша.</span><span class="sxs-lookup"><span data-stu-id="b8582-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="b8582-112">*фашбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8582-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8582-113">Указатель на массив байтов, содержащий хэш.</span><span class="sxs-lookup"><span data-stu-id="b8582-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="b8582-114">*двхашсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8582-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8582-115">Размер массива *фашбитес* в байтах.</span><span class="sxs-lookup"><span data-stu-id="b8582-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="b8582-116">*дворигиналимажесизе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b8582-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8582-117">Размер (в байтах) исходного изображения, из которого был вычислен хэш.</span><span class="sxs-lookup"><span data-stu-id="b8582-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="b8582-118">*пдвфаундлевел* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8582-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8582-119">Указатель на идентификатор уровня для соответствующего правила идентификации хэш-кода.</span><span class="sxs-lookup"><span data-stu-id="b8582-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="b8582-120">*пдвсаферфлагс*</span><span class="sxs-lookup"><span data-stu-id="b8582-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b8582-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="b8582-121">Reserved.</span></span> <span data-ttu-id="b8582-122">Присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="b8582-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8582-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8582-123">Return value</span></span>

<span data-ttu-id="b8582-124">**Значение true** , если функция выполнена успешно; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b8582-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8582-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b8582-125">Requirements</span></span>



| <span data-ttu-id="b8582-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b8582-126">Requirement</span></span> | <span data-ttu-id="b8582-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b8582-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8582-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8582-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b8582-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b8582-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b8582-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8582-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b8582-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8582-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8582-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b8582-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8582-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8582-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 
