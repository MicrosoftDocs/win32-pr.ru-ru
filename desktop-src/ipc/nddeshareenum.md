---
description: Возвращает список доступных общих ресурсов DDE.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Функция Нддешаринум (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693335"
---
# <a name="nddeshareenum-function"></a><span data-ttu-id="2251c-103">Функция Нддешаринум</span><span class="sxs-lookup"><span data-stu-id="2251c-103">NDdeShareEnum function</span></span>

<span data-ttu-id="2251c-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2251c-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="2251c-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="2251c-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="2251c-106">Возвращает список доступных общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="2251c-106">Retrieves the list of available DDE shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="2251c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2251c-107">Syntax</span></span>


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="2251c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2251c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2251c-109">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2251c-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2251c-110">Имя сервера, на котором находится DSDM.</span><span class="sxs-lookup"><span data-stu-id="2251c-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="2251c-111">*нлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2251c-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2251c-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2251c-112">Reserved.</span></span> <span data-ttu-id="2251c-113">Этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2251c-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2251c-114">*лпбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2251c-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2251c-115">Указатель на буфер, который получает список общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="2251c-115">A pointer to a buffer that receives the list of DDE shares.</span></span> <span data-ttu-id="2251c-116">Список общих ресурсов DDE хранится в виде последовательности строк с разделителями null, заканчивающихся символом двойного NULL в конце.</span><span class="sxs-lookup"><span data-stu-id="2251c-116">The list of DDE shares is stored as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="2251c-117">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2251c-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="2251c-118">Если *лпбуффер* имеет **значение NULL**, DSDM возвращает размер буфера, необходимого для хранения списка общих ресурсов в параметре *лпкбтоталаваилабле* .</span><span class="sxs-lookup"><span data-stu-id="2251c-118">If *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2251c-119">*кбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2251c-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2251c-120">Размер буфера *лпбуффер* в байтах.</span><span class="sxs-lookup"><span data-stu-id="2251c-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="2251c-121">Если *лпбуффер* имеет **значение NULL**, этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2251c-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2251c-122">*лпнентриесреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2251c-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2251c-123">Указатель на переменную, которая получает общее число перечислений общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2251c-123">A pointer to a variable that receives the total number of shares being enumerated.</span></span> <span data-ttu-id="2251c-124">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2251c-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2251c-125">*лпкбтоталаваилабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2251c-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2251c-126">Указатель на переменную, которая получает общее число байтов, необходимых в буфере для хранения списка общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="2251c-126">A pointer to a variable that receives the total number of bytes needed in the buffer to store the list of DDE shares.</span></span> <span data-ttu-id="2251c-127">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2251c-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2251c-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2251c-128">Return value</span></span>

<span data-ttu-id="2251c-129">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="2251c-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="2251c-130">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="2251c-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="2251c-131">Если параметр *лпбуффер* имеет **значение NULL**, он возвращает ндде \_ buf \_ слишком \_ мал.</span><span class="sxs-lookup"><span data-stu-id="2251c-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2251c-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2251c-132">Requirements</span></span>



| <span data-ttu-id="2251c-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2251c-133">Requirement</span></span> | <span data-ttu-id="2251c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2251c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2251c-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2251c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2251c-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2251c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2251c-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2251c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2251c-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2251c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2251c-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2251c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2251c-140"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2251c-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="2251c-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2251c-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="2251c-142"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2251c-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2251c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2251c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2251c-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2251c-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="2251c-145">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="2251c-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2251c-146">**Нддешаринумв** (Юникод) и **нддешаринума** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2251c-146">**NDdeShareEnumW** (Unicode) and **NDdeShareEnumA** (ANSI)</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="2251c-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2251c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2251c-148">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="2251c-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="2251c-149">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="2251c-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




