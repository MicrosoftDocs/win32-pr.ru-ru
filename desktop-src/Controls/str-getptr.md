---
title: Функция Str_GetPtr
description: Копирует строку из одного буфера в другой.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Функции Str_GetPtr элементов управления Windows
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801534"
---
# <a name="str_getptr-function"></a><span data-ttu-id="b085a-104">Str \_ жетптр, функция</span><span class="sxs-lookup"><span data-stu-id="b085a-104">Str\_GetPtr function</span></span>

<span data-ttu-id="b085a-105">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b085a-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="b085a-106">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b085a-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b085a-107">Копирует строку из одного буфера в другой.</span><span class="sxs-lookup"><span data-stu-id="b085a-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="b085a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b085a-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="b085a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b085a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b085a-110">*псзсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b085a-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b085a-111">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b085a-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b085a-112">Указатель на исходную строку.</span><span class="sxs-lookup"><span data-stu-id="b085a-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="b085a-113">*псздест* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b085a-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b085a-114">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b085a-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b085a-115">Указатель на целевой буфер.</span><span class="sxs-lookup"><span data-stu-id="b085a-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="b085a-116">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="b085a-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b085a-117">*кчдест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b085a-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b085a-118">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="b085a-118">Type: **int**</span></span>

<span data-ttu-id="b085a-119">Размер *псздест* в символах.</span><span class="sxs-lookup"><span data-stu-id="b085a-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b085a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b085a-120">Return value</span></span>

<span data-ttu-id="b085a-121">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="b085a-121">Type: **int**</span></span>

<span data-ttu-id="b085a-122">Если *псздест* имеет **значение NULL** или *кчдест* равен нулю, возвращает размер буфера (в символах), который должен содержать завершающуюся нулем копию строки, на которую указывает *псзсаурце*.</span><span class="sxs-lookup"><span data-stu-id="b085a-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="b085a-123">Если *псздест* имеет значение, отличное от **null**, возвращает число успешно скопированных символов, включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="b085a-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="b085a-124">Если *псздест* не может вместить всю строку, на которую указывает *псзсаурце*, то символы (*кчдест*-1) копируются, строка, заканчивающаяся нулем, и *кчдест* возвращается.</span><span class="sxs-lookup"><span data-stu-id="b085a-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b085a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b085a-125">Remarks</span></span>

<span data-ttu-id="b085a-126">**Str \_ Жетптр** доступен в виде версий ANSI (**str \_ Жетптра**) и Unicode (**str \_ жетптрв**).</span><span class="sxs-lookup"><span data-stu-id="b085a-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="b085a-127">Эти функции не экспортируются по имени или объявляются в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="b085a-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="b085a-128">Чтобы использовать их, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 233 (**str \_ жетптра**) или 235 (**str \_ жетптрв**) из ComCtl32.dll, чтобы получить указатель на функцию.</span><span class="sxs-lookup"><span data-stu-id="b085a-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b085a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b085a-129">Requirements</span></span>



| <span data-ttu-id="b085a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b085a-130">Requirement</span></span> | <span data-ttu-id="b085a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b085a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b085a-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b085a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b085a-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b085a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b085a-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b085a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b085a-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b085a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b085a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b085a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b085a-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b085a-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="b085a-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b085a-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b085a-139">**Str \_ Жетптрв** (Юникод) и **str \_ жетптра** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b085a-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

