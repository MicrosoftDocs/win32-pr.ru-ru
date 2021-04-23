---
description: Функция Жетфрамемачеадерленгс возвращает длину (в байтах) заголовка MAC кадра.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Функция Жетфрамемачеадерленгс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650478"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="34fcb-103">Функция Жетфрамемачеадерленгс</span><span class="sxs-lookup"><span data-stu-id="34fcb-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="34fcb-104">Функция **жетфрамемачеадерленгс** возвращает длину (в байтах) заголовка Mac кадра.</span><span class="sxs-lookup"><span data-stu-id="34fcb-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fcb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34fcb-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="34fcb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34fcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34fcb-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34fcb-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34fcb-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="34fcb-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34fcb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34fcb-109">Return value</span></span>

<span data-ttu-id="34fcb-110">Если функция выполнена успешно, возвращаемое значение представляет собой длину заголовка MAC в байтах.</span><span class="sxs-lookup"><span data-stu-id="34fcb-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="34fcb-111">Если функция не выполнена или обнаружен неизвестный тип MAC, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="34fcb-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="34fcb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34fcb-112">Remarks</span></span>

<span data-ttu-id="34fcb-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамемачеадерленгс** .</span><span class="sxs-lookup"><span data-stu-id="34fcb-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34fcb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="34fcb-114">Requirements</span></span>



| <span data-ttu-id="34fcb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="34fcb-115">Requirement</span></span> | <span data-ttu-id="34fcb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="34fcb-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="34fcb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34fcb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="34fcb-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34fcb-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="34fcb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34fcb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="34fcb-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34fcb-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="34fcb-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="34fcb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="34fcb-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="34fcb-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="34fcb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34fcb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="34fcb-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34fcb-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="34fcb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="34fcb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34fcb-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34fcb-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




