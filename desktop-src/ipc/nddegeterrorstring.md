---
description: Преобразует код ошибки, возвращенный сетевой функцией DDE, в строку ошибки, объясняющую возвращенный код ошибки.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Функция Нддежетеррорстринг (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072607"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="005f6-103">Функция Нддежетеррорстринг</span><span class="sxs-lookup"><span data-stu-id="005f6-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="005f6-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="005f6-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="005f6-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="005f6-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="005f6-106">Преобразует код ошибки, возвращенный сетевой функцией DDE, в строку ошибки, объясняющую возвращенный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="005f6-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="005f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="005f6-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="005f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="005f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005f6-109">*уерроркоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="005f6-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005f6-110">Код ошибки для преобразования в строку ошибки.</span><span class="sxs-lookup"><span data-stu-id="005f6-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="005f6-111">*лпсзеррорстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="005f6-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="005f6-112">Указатель на буфер, который получает переведенную строку ошибки.</span><span class="sxs-lookup"><span data-stu-id="005f6-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="005f6-113">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="005f6-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="005f6-114">Если буфер недостаточно велик для хранения полной строки ошибки, строка усекается.</span><span class="sxs-lookup"><span data-stu-id="005f6-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="005f6-115">*кбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="005f6-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005f6-116">Размер буфера для получения строки ошибки в **тчарс**.</span><span class="sxs-lookup"><span data-stu-id="005f6-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005f6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="005f6-117">Return value</span></span>

<span data-ttu-id="005f6-118">Если вызов функции заканчивается удачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="005f6-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="005f6-119">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="005f6-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="005f6-120">Если буфер *лпсзеррорстринг* не достаточен для приема всей строки ошибки, а строка усекается, функция ВОЗВРАЩАЕТ значение ндде \_ Внутренняя \_ ошибка.</span><span class="sxs-lookup"><span data-stu-id="005f6-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="005f6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="005f6-121">Requirements</span></span>



| <span data-ttu-id="005f6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="005f6-122">Requirement</span></span> | <span data-ttu-id="005f6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="005f6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="005f6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="005f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="005f6-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="005f6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="005f6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="005f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="005f6-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="005f6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="005f6-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="005f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="005f6-129"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="005f6-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="005f6-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="005f6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="005f6-131"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="005f6-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="005f6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="005f6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="005f6-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="005f6-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="005f6-134">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="005f6-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="005f6-135">**Нддежетеррорстрингв** (Юникод) и **нддежетеррорстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="005f6-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="005f6-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="005f6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005f6-137">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="005f6-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="005f6-138">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="005f6-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




