---
description: 'Принимает структуру СТРРЕТ, возвращенную Ишеллфолдер:: Жетдисплайнамеоф, преобразует ее в строку и помещает результат в буфер.'
title: Функция Стрреттострн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997954"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="02f9a-103">Функция Стрреттострн</span><span class="sxs-lookup"><span data-stu-id="02f9a-103">StrRetToStrN function</span></span>

<span data-ttu-id="02f9a-104">Принимает структуру [**стррет**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , возвращенную [**Ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), преобразует ее в строку и помещает результат в буфер.</span><span class="sxs-lookup"><span data-stu-id="02f9a-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02f9a-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="02f9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02f9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f9a-107">*псзаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02f9a-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02f9a-108">Тип: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="02f9a-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="02f9a-109">Буфер для хранения отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="02f9a-109">Buffer to hold the display name.</span></span> <span data-ttu-id="02f9a-110">Он будет возвращен в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="02f9a-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="02f9a-111">Если *кчаут* слишком мал, имя будет обрезано до размера.</span><span class="sxs-lookup"><span data-stu-id="02f9a-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="02f9a-112">*кчаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02f9a-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f9a-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="02f9a-113">Type: **UINT**</span></span>

<span data-ttu-id="02f9a-114">Размер *псзаут* в символах.</span><span class="sxs-lookup"><span data-stu-id="02f9a-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="02f9a-115">Если *кчаут* слишком мал, строка будет обрезана до размера.</span><span class="sxs-lookup"><span data-stu-id="02f9a-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="02f9a-116">*пстррет* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="02f9a-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02f9a-117">Тип: **лпстррет**</span><span class="sxs-lookup"><span data-stu-id="02f9a-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="02f9a-118">Указатель на структуру [**стррет**](/windows/desktop/api/Shtypes/ns-shtypes-strret) .</span><span class="sxs-lookup"><span data-stu-id="02f9a-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="02f9a-119">Когда функция возвращает, этот указатель больше не будет действительным.</span><span class="sxs-lookup"><span data-stu-id="02f9a-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="02f9a-120">*Пидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02f9a-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f9a-121">Тип: **лпЦитемидлист**</span><span class="sxs-lookup"><span data-stu-id="02f9a-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="02f9a-122">Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) элемента.</span><span class="sxs-lookup"><span data-stu-id="02f9a-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f9a-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02f9a-123">Return value</span></span>

<span data-ttu-id="02f9a-124">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="02f9a-124">Type: **BOOL**</span></span>

<span data-ttu-id="02f9a-125">**True** для успешного выполнения, **false** для сбоя.</span><span class="sxs-lookup"><span data-stu-id="02f9a-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f9a-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="02f9a-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02f9a-127">Начиная с версии Shell32.dll 5,0, вызов этой функции эквивалентен вызову [**стрреттобуф**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span><span class="sxs-lookup"><span data-stu-id="02f9a-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="02f9a-128">**Стрреттострн** не экспортируется по имени.</span><span class="sxs-lookup"><span data-stu-id="02f9a-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="02f9a-129">Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 96 из Shell32.dll для получения указателя на функцию.</span><span class="sxs-lookup"><span data-stu-id="02f9a-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="02f9a-130">Если элемент **утипе** структуры, на который указывает *пстррет* , имеет значение **Стррет \_ встр**, то элемент **полестр** этой структуры будет освобожден при возврате.</span><span class="sxs-lookup"><span data-stu-id="02f9a-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="02f9a-131">Обратите внимание, что эта функция экспортируется из Shell32.dll, а не Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="02f9a-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="02f9a-132">Он также включается в Шлобж. h, а не в Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="02f9a-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f9a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="02f9a-133">Requirements</span></span>



| <span data-ttu-id="02f9a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="02f9a-134">Requirement</span></span> | <span data-ttu-id="02f9a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="02f9a-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f9a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02f9a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="02f9a-137">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="02f9a-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="02f9a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02f9a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="02f9a-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02f9a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02f9a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="02f9a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02f9a-141"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="02f9a-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f9a-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02f9a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f9a-143">**стрреттостр**</span><span class="sxs-lookup"><span data-stu-id="02f9a-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="02f9a-144">**стрреттобуф**</span><span class="sxs-lookup"><span data-stu-id="02f9a-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
