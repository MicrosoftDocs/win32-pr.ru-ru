---
description: Удаляет общую папку DDE из диспетчера общей базы данных DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Функция Нддешаредел (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682433"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="11b14-103">Функция Нддешаредел</span><span class="sxs-lookup"><span data-stu-id="11b14-103">NDdeShareDel function</span></span>

<span data-ttu-id="11b14-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="11b14-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="11b14-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="11b14-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="11b14-106">Удаляет общую папку DDE из диспетчера общей базы данных DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="11b14-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="11b14-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11b14-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="11b14-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11b14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11b14-109">*лпсзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11b14-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b14-110">Имя сервера, DSDM которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="11b14-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="11b14-111">*лпсзшаренаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11b14-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b14-112">Имя общего ресурса, удаляемого из DSDM.</span><span class="sxs-lookup"><span data-stu-id="11b14-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="11b14-113">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="11b14-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11b14-114">*вресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11b14-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b14-115">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="11b14-115">Reserved.</span></span> <span data-ttu-id="11b14-116">Этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="11b14-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11b14-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11b14-117">Return value</span></span>

<span data-ttu-id="11b14-118">Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="11b14-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="11b14-119">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="11b14-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11b14-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11b14-120">Remarks</span></span>

<span data-ttu-id="11b14-121">Чтобы удалить общий ресурс DDE из DSDM, необходимо иметь соответствующие права доступа.</span><span class="sxs-lookup"><span data-stu-id="11b14-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="11b14-122">Автор общего ресурса имеет право на удаление.</span><span class="sxs-lookup"><span data-stu-id="11b14-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="11b14-123">Требования</span><span class="sxs-lookup"><span data-stu-id="11b14-123">Requirements</span></span>



| <span data-ttu-id="11b14-124">Требование</span><span class="sxs-lookup"><span data-stu-id="11b14-124">Requirement</span></span> | <span data-ttu-id="11b14-125">Значение</span><span class="sxs-lookup"><span data-stu-id="11b14-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11b14-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11b14-126">Minimum supported client</span></span><br/> | <span data-ttu-id="11b14-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11b14-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="11b14-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11b14-128">Minimum supported server</span></span><br/> | <span data-ttu-id="11b14-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11b14-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="11b14-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11b14-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="11b14-131"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="11b14-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="11b14-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11b14-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="11b14-133"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11b14-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="11b14-134">DLL</span><span class="sxs-lookup"><span data-stu-id="11b14-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b14-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11b14-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="11b14-136">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="11b14-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11b14-137">**Нддешаределв** (Юникод) и **нддешаредела** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11b14-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="11b14-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11b14-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b14-139">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="11b14-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="11b14-140">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="11b14-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




