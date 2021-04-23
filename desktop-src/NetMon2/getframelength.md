---
description: Функция Жетфрамеленгс возвращает длину кадра.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Функция Жетфрамеленгс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662187"
---
# <a name="getframelength-function"></a><span data-ttu-id="75244-103">Функция Жетфрамеленгс</span><span class="sxs-lookup"><span data-stu-id="75244-103">GetFrameLength function</span></span>

<span data-ttu-id="75244-104">Функция **жетфрамеленгс** возвращает длину кадра.</span><span class="sxs-lookup"><span data-stu-id="75244-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="75244-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75244-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="75244-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75244-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75244-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75244-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="75244-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75244-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75244-109">Return value</span></span>

<span data-ttu-id="75244-110">Если функция выполнена успешно, возвращаемое значение равно длине кадра в байтах.</span><span class="sxs-lookup"><span data-stu-id="75244-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="75244-111">Если функция завершилась неудачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="75244-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="75244-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75244-112">Remarks</span></span>

<span data-ttu-id="75244-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамеленгс** .</span><span class="sxs-lookup"><span data-stu-id="75244-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="75244-114">Требования</span><span class="sxs-lookup"><span data-stu-id="75244-114">Requirements</span></span>



| <span data-ttu-id="75244-115">Требование</span><span class="sxs-lookup"><span data-stu-id="75244-115">Requirement</span></span> | <span data-ttu-id="75244-116">Значение</span><span class="sxs-lookup"><span data-stu-id="75244-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75244-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75244-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75244-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="75244-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75244-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75244-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75244-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="75244-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75244-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="75244-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="75244-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="75244-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="75244-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="75244-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="75244-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75244-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="75244-125">DLL</span><span class="sxs-lookup"><span data-stu-id="75244-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75244-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75244-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




