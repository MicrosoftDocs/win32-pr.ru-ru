---
description: Извлекает сведения об общем ресурсе DDE. Обычно это делается для редактирования.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Функция Нддешарежетинфо (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682432"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="b5ec7-104">Функция Нддешарежетинфо</span><span class="sxs-lookup"><span data-stu-id="b5ec7-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="b5ec7-105">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b5ec7-106">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b5ec7-107">Извлекает сведения об общем ресурсе DDE.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-107">Retrieves DDE share information.</span></span> <span data-ttu-id="b5ec7-108">Обычно это делается для редактирования.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ec7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5ec7-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="b5ec7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5ec7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ec7-111">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-112">Имя сервера, на котором находится DSDM.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec7-113">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-114">Имя общего ресурса, сведения о котором необходимо получить из DSDM.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="b5ec7-115">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec7-116">*нлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-117">Уровень информации.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-117">The information level.</span></span> <span data-ttu-id="b5ec7-118">Этот параметр должен быть равен 2.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec7-119">*лпбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-120">Указатель на буфер, который получает структуру [**нддешареинфо**](nddeshareinfo-str.md) и связанные данные, на которые указывает элемент.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="b5ec7-121">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="b5ec7-122">Если *лпбуффер* имеет **значение NULL**, то DSDM вычисляет число байтов, необходимых для хранения запрашиваемой информации об общем ресурсе, и возвращает это значение в поле *лпнтоталаваилабле* вместе с ндде \_ buf \_ слишком \_ маленькой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec7-123">*кбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-124">Размер буфера *лпбуффер* в байтах.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="b5ec7-125">Если *лпбуффер* имеет **значение NULL**, *кбуфсизе* должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec7-126">*лпнтоталаваилабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-127">Указатель на переменную, которая получает общее число байтов, необходимых для хранения запрошенных сведений об общем ресурсе.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="b5ec7-128">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5ec7-129">*лпнитемс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ec7-130">Указатель на маску выделения элемента для частичного извлечения сведений общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ec7-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5ec7-131">Return value</span></span>

<span data-ttu-id="b5ec7-132">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="b5ec7-133">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="b5ec7-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="b5ec7-134">Если параметр *лпбуффер* имеет **значение NULL**, он возвращает ндде \_ buf \_ слишком \_ мал.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ec7-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b5ec7-135">Requirements</span></span>



| <span data-ttu-id="b5ec7-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b5ec7-136">Requirement</span></span> | <span data-ttu-id="b5ec7-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ec7-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ec7-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5ec7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ec7-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b5ec7-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5ec7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ec7-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5ec7-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5ec7-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b5ec7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ec7-143"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ec7-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5ec7-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5ec7-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5ec7-145"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5ec7-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5ec7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ec7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ec7-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ec7-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5ec7-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b5ec7-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b5ec7-149">**Нддешарежетинфов** (Юникод) и **нддешарежетинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b5ec7-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b5ec7-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5ec7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ec7-151">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="b5ec7-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b5ec7-152">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="b5ec7-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b5ec7-153">**нддешареинфо**</span><span class="sxs-lookup"><span data-stu-id="b5ec7-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="b5ec7-154">**нддешаресетинфо**</span><span class="sxs-lookup"><span data-stu-id="b5ec7-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




