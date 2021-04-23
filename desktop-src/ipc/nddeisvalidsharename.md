---
description: Определяет, использует ли имя общего ресурса правильный синтаксис.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Функция Нддеисвалидшаренаме (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682434"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="f4dfe-103">Функция Нддеисвалидшаренаме</span><span class="sxs-lookup"><span data-stu-id="f4dfe-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="f4dfe-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="f4dfe-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="f4dfe-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="f4dfe-106">Определяет, использует ли имя общего ресурса правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4dfe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4dfe-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="f4dfe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4dfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4dfe-109">*имя_общего_ресурса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4dfe-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4dfe-110">Имя общей папки для проверки.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-110">The share name to be validated.</span></span> <span data-ttu-id="f4dfe-111">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4dfe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4dfe-112">Return value</span></span>

<span data-ttu-id="f4dfe-113">Если имя общего ресурса имеет допустимый синтаксис, то возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="f4dfe-114">Если имя общего ресурса не имеет допустимого синтаксиса, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4dfe-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4dfe-115">Remarks</span></span>

<span data-ttu-id="f4dfe-116">Эта функция также вызывается [**нддешареадд**](nddeshareadd.md) при создании общего ресурса DDE.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4dfe-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f4dfe-117">Requirements</span></span>



| <span data-ttu-id="f4dfe-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f4dfe-118">Requirement</span></span> | <span data-ttu-id="f4dfe-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f4dfe-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4dfe-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4dfe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4dfe-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f4dfe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4dfe-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4dfe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4dfe-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f4dfe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f4dfe-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f4dfe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4dfe-125"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4dfe-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4dfe-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4dfe-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4dfe-127"><dt>Нддеапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4dfe-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f4dfe-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f4dfe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4dfe-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4dfe-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4dfe-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f4dfe-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f4dfe-131">**Нддеисвалидшаренамев** (Юникод) и **нддеисвалидшаренамеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f4dfe-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="f4dfe-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4dfe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4dfe-133">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="f4dfe-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="f4dfe-134">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="f4dfe-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="f4dfe-135">**нддешареадд**</span><span class="sxs-lookup"><span data-stu-id="f4dfe-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




