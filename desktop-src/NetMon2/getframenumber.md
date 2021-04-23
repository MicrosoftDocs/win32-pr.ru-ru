---
description: Функция Жетфраменумбер возвращает номер кадра.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Функция Жетфраменумбер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990903"
---
# <a name="getframenumber-function"></a><span data-ttu-id="35fb9-103">Функция Жетфраменумбер</span><span class="sxs-lookup"><span data-stu-id="35fb9-103">GetFrameNumber function</span></span>

<span data-ttu-id="35fb9-104">Функция **жетфраменумбер** возвращает номер кадра.</span><span class="sxs-lookup"><span data-stu-id="35fb9-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35fb9-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="35fb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35fb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fb9-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35fb9-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fb9-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="35fb9-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fb9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35fb9-109">Return value</span></span>

<span data-ttu-id="35fb9-110">Если функция выполнена успешно, возвращаемое значение является номером кадра, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="35fb9-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="35fb9-111">Если функция не выполнена успешно, возвращаемое значение равно минус единице (-1).</span><span class="sxs-lookup"><span data-stu-id="35fb9-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="35fb9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35fb9-112">Remarks</span></span>

<span data-ttu-id="35fb9-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфраменумбер** .</span><span class="sxs-lookup"><span data-stu-id="35fb9-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fb9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="35fb9-114">Requirements</span></span>



| <span data-ttu-id="35fb9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="35fb9-115">Requirement</span></span> | <span data-ttu-id="35fb9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="35fb9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35fb9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35fb9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35fb9-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35fb9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="35fb9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35fb9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35fb9-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35fb9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35fb9-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="35fb9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fb9-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="35fb9-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="35fb9-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35fb9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="35fb9-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35fb9-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="35fb9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35fb9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35fb9-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35fb9-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




