---
description: Задает общие сведения об общем ресурсе DDE. Обычно это выполняется после редактирования.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Функция Нддешаресетинфо (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682431"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="c1c4e-104">Функция Нддешаресетинфо</span><span class="sxs-lookup"><span data-stu-id="c1c4e-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="c1c4e-105">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="c1c4e-106">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="c1c4e-107">Задает общие сведения об общем ресурсе DDE.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-107">Sets DDE share information.</span></span> <span data-ttu-id="c1c4e-108">Обычно это выполняется после редактирования.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c4e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1c4e-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="c1c4e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1c4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c4e-111">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4e-112">Имя сервера, DSDM которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="c1c4e-113">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4e-114">Имя общего ресурса, сведения о котором необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="c1c4e-115">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1c4e-116">*нлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4e-117">Уровень информации.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-117">The information level.</span></span> <span data-ttu-id="c1c4e-118">Этот параметр должен быть равен 2.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="c1c4e-119">*lpBuffer* \[ввод\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4e-120">Указатель на структуру [**нддешареинфо**](nddeshareinfo-str.md) , указывающий общую информацию DDE, которая должна храниться в DSDM.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="c1c4e-121">В настоящее время общие сведения об общем ресурсе DDE изменяются целиком, то есть частичные изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="c1c4e-122">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1c4e-123">*кбуфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4e-124">Размер буфера *лпбуффер* в байтах.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c1c4e-125">*спармнум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4e-126">Изменяемый индекс параметра.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-126">The parameter index to be modified.</span></span> <span data-ttu-id="c1c4e-127">Текущая реализация не поддерживает частичное изменение; Поэтому этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c4e-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1c4e-128">Return value</span></span>

<span data-ttu-id="c1c4e-129">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="c1c4e-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="c1c4e-130">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="c1c4e-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c4e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c1c4e-131">Requirements</span></span>



| <span data-ttu-id="c1c4e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c1c4e-132">Requirement</span></span> | <span data-ttu-id="c1c4e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c1c4e-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c4e-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1c4e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c4e-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c1c4e-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1c4e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c4e-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1c4e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1c4e-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c1c4e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c4e-139"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c4e-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1c4e-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1c4e-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1c4e-141"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1c4e-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1c4e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c4e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c4e-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c4e-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1c4e-144">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c1c4e-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c1c4e-145">**Нддешаресетинфов** (Юникод) и **нддешаресетинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c1c4e-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c1c4e-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1c4e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c4e-147">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="c1c4e-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="c1c4e-148">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="c1c4e-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="c1c4e-149">**нддешареинфо**</span><span class="sxs-lookup"><span data-stu-id="c1c4e-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="c1c4e-150">**нддешарежетинфо**</span><span class="sxs-lookup"><span data-stu-id="c1c4e-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




