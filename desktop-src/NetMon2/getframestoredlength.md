---
description: Функция Жетфраместоредленгс возвращает длину кадра.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Функция Жетфраместоредленгс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674090"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="f2ce3-103">Функция Жетфраместоредленгс</span><span class="sxs-lookup"><span data-stu-id="f2ce3-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="f2ce3-104">Функция **жетфраместоредленгс** возвращает длину кадра.</span><span class="sxs-lookup"><span data-stu-id="f2ce3-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ce3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2ce3-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f2ce3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2ce3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ce3-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2ce3-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ce3-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="f2ce3-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ce3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2ce3-109">Return value</span></span>

<span data-ttu-id="f2ce3-110">Если функция выполнена успешно, возвращаемое значение — это длина фрейма, которая сохраняется.</span><span class="sxs-lookup"><span data-stu-id="f2ce3-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="f2ce3-111">Если функция завершилась неудачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f2ce3-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ce3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2ce3-112">Remarks</span></span>

<span data-ttu-id="f2ce3-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфраместоредленгс** .</span><span class="sxs-lookup"><span data-stu-id="f2ce3-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ce3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f2ce3-114">Requirements</span></span>



| <span data-ttu-id="f2ce3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f2ce3-115">Requirement</span></span> | <span data-ttu-id="f2ce3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ce3-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ce3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2ce3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ce3-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2ce3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f2ce3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2ce3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ce3-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2ce3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2ce3-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f2ce3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ce3-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ce3-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f2ce3-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2ce3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2ce3-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2ce3-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2ce3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f2ce3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2ce3-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2ce3-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ce3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2ce3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ce3-128">жетфрамеленгс</span><span class="sxs-lookup"><span data-stu-id="f2ce3-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




