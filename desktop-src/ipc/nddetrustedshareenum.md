---
description: Возвращает имена всех общих сетевых ресурсов DDE, которые являются доверенными в контексте вызывающего процесса.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Функция Нддетрустедшаринум (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348245"
---
# <a name="nddetrustedshareenum-function"></a><span data-ttu-id="edd63-103">Функция Нддетрустедшаринум</span><span class="sxs-lookup"><span data-stu-id="edd63-103">NDdeTrustedShareEnum function</span></span>

<span data-ttu-id="edd63-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="edd63-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="edd63-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="edd63-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="edd63-106">Возвращает имена всех общих сетевых ресурсов DDE, которые являются доверенными в контексте вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="edd63-106">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd63-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edd63-107">Syntax</span></span>


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="edd63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="edd63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd63-109">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edd63-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd63-110">Имя сервера, на котором находится DSDM.</span><span class="sxs-lookup"><span data-stu-id="edd63-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="edd63-111">*нлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edd63-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd63-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="edd63-112">Reserved.</span></span> <span data-ttu-id="edd63-113">Этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="edd63-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="edd63-114">*лпбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="edd63-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd63-115">Указатель на буфер, который получает список доверенных общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="edd63-115">A pointer to a buffer that receives the list of trusted DDE shares.</span></span> <span data-ttu-id="edd63-116">Список доверенных общих ресурсов DDE возвращается в виде последовательности строк с разделителями null, заканчивающихся символом двойного NULL в конце.</span><span class="sxs-lookup"><span data-stu-id="edd63-116">The list of trusted DDE shares is returned as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="edd63-117">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="edd63-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="edd63-118">Если *лпбуффер* имеет **значение NULL**, DSDM возвращает размер буфера, необходимого для хранения списка общих ресурсов в поле *лпкбтоталаваилабле* .</span><span class="sxs-lookup"><span data-stu-id="edd63-118">If the *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* field.</span></span>

</dd> <dt>

<span data-ttu-id="edd63-119">*кбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edd63-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd63-120">Размер буфера *лпбуффер* в байтах.</span><span class="sxs-lookup"><span data-stu-id="edd63-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="edd63-121">Если *лпбуффер* имеет **значение NULL**, этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="edd63-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="edd63-122">*лпнентриесреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="edd63-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd63-123">Указатель на переменную, которая получает общее число перечислений доверенных общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edd63-123">A pointer to a variable that receives the total number of trusted shares being enumerated.</span></span> <span data-ttu-id="edd63-124">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="edd63-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="edd63-125">*лпкбтоталаваилабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="edd63-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edd63-126">Указатель на переменную, которая получает общее число байтов, необходимых для хранения списка доверенных общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="edd63-126">A pointer to a variable that receives the total number of bytes needed to store the list of trusted DDE shares.</span></span> <span data-ttu-id="edd63-127">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="edd63-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd63-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edd63-128">Return value</span></span>

<span data-ttu-id="edd63-129">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="edd63-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="edd63-130">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="edd63-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="edd63-131">Если параметр *лпбуффер* имеет **значение NULL**, он возвращает ндде \_ buf \_ слишком \_ мал.</span><span class="sxs-lookup"><span data-stu-id="edd63-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd63-132">Требования</span><span class="sxs-lookup"><span data-stu-id="edd63-132">Requirements</span></span>



| <span data-ttu-id="edd63-133">Требование</span><span class="sxs-lookup"><span data-stu-id="edd63-133">Requirement</span></span> | <span data-ttu-id="edd63-134">Значение</span><span class="sxs-lookup"><span data-stu-id="edd63-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edd63-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edd63-135">Minimum supported client</span></span><br/> | <span data-ttu-id="edd63-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="edd63-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="edd63-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edd63-137">Minimum supported server</span></span><br/> | <span data-ttu-id="edd63-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="edd63-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="edd63-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="edd63-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd63-140"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="edd63-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="edd63-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="edd63-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="edd63-142"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edd63-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="edd63-143">DLL</span><span class="sxs-lookup"><span data-stu-id="edd63-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd63-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd63-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="edd63-145">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="edd63-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="edd63-146">**Нддетрустедшаринумв** (Юникод) и **нддетрустедшаринума** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="edd63-146">**NDdeTrustedShareEnumW** (Unicode) and **NDdeTrustedShareEnumA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="edd63-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edd63-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd63-148">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="edd63-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="edd63-149">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="edd63-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




