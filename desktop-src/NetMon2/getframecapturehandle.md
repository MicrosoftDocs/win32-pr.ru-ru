---
description: Функция Жетфрамекаптурехандле возвращает маркер записи на основе данного кадра.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Функция Жетфрамекаптурехандле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896778"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="fada1-103">Функция Жетфрамекаптурехандле</span><span class="sxs-lookup"><span data-stu-id="fada1-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="fada1-104">Функция **жетфрамекаптурехандле** возвращает маркер записи на основе данного кадра.</span><span class="sxs-lookup"><span data-stu-id="fada1-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="fada1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fada1-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="fada1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fada1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fada1-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fada1-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fada1-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="fada1-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fada1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fada1-109">Return value</span></span>

<span data-ttu-id="fada1-110">Если функция выполнена успешно, возвращаемое значение является маркером записи.</span><span class="sxs-lookup"><span data-stu-id="fada1-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="fada1-111">Если функция завершается неудачно, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="fada1-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="fada1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fada1-112">Remarks</span></span>

<span data-ttu-id="fada1-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамекаптурехандле** .</span><span class="sxs-lookup"><span data-stu-id="fada1-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fada1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fada1-114">Requirements</span></span>



| <span data-ttu-id="fada1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fada1-115">Requirement</span></span> | <span data-ttu-id="fada1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fada1-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fada1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fada1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fada1-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fada1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fada1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fada1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fada1-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fada1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fada1-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fada1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fada1-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fada1-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fada1-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fada1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="fada1-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fada1-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fada1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fada1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fada1-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fada1-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




