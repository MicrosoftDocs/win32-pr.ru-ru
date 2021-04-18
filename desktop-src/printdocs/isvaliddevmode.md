---
description: Функция Исвалиддевмоде проверяет допустимость содержимого структуры DEVMODE.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Функция Исвалиддевмоде (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719707"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="6d21f-103">Функция Исвалиддевмоде</span><span class="sxs-lookup"><span data-stu-id="6d21f-103">IsValidDevmode function</span></span>

<span data-ttu-id="6d21f-104">Функция **исвалиддевмоде** проверяет допустимость содержимого структуры DEVMODE.</span><span class="sxs-lookup"><span data-stu-id="6d21f-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d21f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d21f-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="6d21f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d21f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d21f-107">*пдевмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d21f-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d21f-108">Указатель на [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) для проверки.</span><span class="sxs-lookup"><span data-stu-id="6d21f-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="6d21f-109">*девмодесизе*</span><span class="sxs-lookup"><span data-stu-id="6d21f-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21f-110">Размер входного буфера байтов в байтах.</span><span class="sxs-lookup"><span data-stu-id="6d21f-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d21f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d21f-111">Return value</span></span>

<span data-ttu-id="6d21f-112">**Значение true**, если [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) имеет структурную допустимую структуру.</span><span class="sxs-lookup"><span data-stu-id="6d21f-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="6d21f-113">Если обнаружены незначительные ошибки, функция исправит их и возвратит **значение true**.</span><span class="sxs-lookup"><span data-stu-id="6d21f-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="6d21f-114">**Значение false**, если [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) имеет одну или несколько серьезных проблем с структурой.</span><span class="sxs-lookup"><span data-stu-id="6d21f-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="6d21f-115">Например, элемент **дмсизе** имеет неправильное соответствие или указывает буфер, который слишком мал.</span><span class="sxs-lookup"><span data-stu-id="6d21f-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="6d21f-116">Кроме того, **значение false** , если **Пдевмоде** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d21f-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d21f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d21f-117">Remarks</span></span>

<span data-ttu-id="6d21f-118">Не проверяются поля частного драйвера принтера [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , а только открытые поля.</span><span class="sxs-lookup"><span data-stu-id="6d21f-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="6d21f-119">Вызывающие объекты должны использовать **дмсизе** + **дмдриверекстра** для **девмодесизе** , только если они гарантируют, что размер входного буфера по крайней мере такой большой.</span><span class="sxs-lookup"><span data-stu-id="6d21f-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="6d21f-120">Так как [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) является обычно ненадежными данными, значения, которые находятся во входном буфере на смещениях **дмсизе** и **дмдриверекстра** , также не являются доверенными.</span><span class="sxs-lookup"><span data-stu-id="6d21f-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="6d21f-121">Эта функция является исполняемым в контексте Least-Privileged учетной записи пользователя (LUA).</span><span class="sxs-lookup"><span data-stu-id="6d21f-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d21f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6d21f-122">Requirements</span></span>



| <span data-ttu-id="6d21f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6d21f-123">Requirement</span></span> | <span data-ttu-id="6d21f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6d21f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d21f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d21f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d21f-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6d21f-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6d21f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d21f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d21f-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d21f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d21f-129">Header</span><span class="sxs-lookup"><span data-stu-id="6d21f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d21f-130"><dt>Винспул. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d21f-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d21f-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d21f-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d21f-132"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d21f-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d21f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6d21f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d21f-134"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6d21f-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="6d21f-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6d21f-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6d21f-136">**Исвалиддевмодев** (Юникод) и **исвалиддевмодеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6d21f-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6d21f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d21f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d21f-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="6d21f-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6d21f-139">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="6d21f-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6d21f-140">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="6d21f-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




