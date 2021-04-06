---
description: Функция Жеткаптуретоталфрамес возвращает общее число кадров в записи.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Функция Жеткаптуретоталфрамес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896782"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="42af6-103">Функция Жеткаптуретоталфрамес</span><span class="sxs-lookup"><span data-stu-id="42af6-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="42af6-104">Функция **жеткаптуретоталфрамес** возвращает общее число кадров в записи.</span><span class="sxs-lookup"><span data-stu-id="42af6-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="42af6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42af6-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="42af6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42af6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42af6-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42af6-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42af6-108">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="42af6-108">Handle to the capture.</span></span> <span data-ttu-id="42af6-109">Дополнительные сведения о получении маркера записи см. в подразделе "Примечания" этой статьи **жеткаптуретоталфрамес** .</span><span class="sxs-lookup"><span data-stu-id="42af6-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42af6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42af6-110">Return value</span></span>

<span data-ttu-id="42af6-111">Если функция выполнена успешно, возвращаемое значение — это общее число кадров в записи.</span><span class="sxs-lookup"><span data-stu-id="42af6-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="42af6-112">Если функция завершается неудачно, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="42af6-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="42af6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42af6-113">Remarks</span></span>

<span data-ttu-id="42af6-114">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптуретоталфрамес** .</span><span class="sxs-lookup"><span data-stu-id="42af6-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="42af6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="42af6-115">Requirements</span></span>



| <span data-ttu-id="42af6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="42af6-116">Requirement</span></span> | <span data-ttu-id="42af6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="42af6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42af6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42af6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42af6-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42af6-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="42af6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42af6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42af6-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42af6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42af6-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42af6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42af6-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="42af6-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="42af6-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42af6-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="42af6-125"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42af6-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="42af6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="42af6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42af6-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42af6-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




