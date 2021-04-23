---
description: Функция Виаадддевице вызывает пользовательский интерфейс мастера установки сканера и камеры. Он эквивалентен запуску &\# 0034; rundll32.exe сти \_ci.dll AddDevice&\# 0034; из командной строки.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Функция Виаадддевице (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809964"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="60c73-104">Функция Виаадддевице</span><span class="sxs-lookup"><span data-stu-id="60c73-104">WiaAddDevice function</span></span>

<span data-ttu-id="60c73-105">Функция **виаадддевице** вызывает пользовательский интерфейс мастера установки сканера и камеры.</span><span class="sxs-lookup"><span data-stu-id="60c73-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="60c73-106">Он эквивалентен запуску "rundll32.exe сти \_ci.dll AddDevice" из командной строки.</span><span class="sxs-lookup"><span data-stu-id="60c73-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c73-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60c73-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="60c73-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60c73-108">Parameters</span></span>

<span data-ttu-id="60c73-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="60c73-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60c73-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60c73-110">Return value</span></span>

<span data-ttu-id="60c73-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="60c73-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60c73-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60c73-112">Remarks</span></span>

<span data-ttu-id="60c73-113">Эта функция должна вызываться с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="60c73-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="60c73-114">При работе в режиме управления учетными записями пользователей (LUA) процесс должен быть повышен.</span><span class="sxs-lookup"><span data-stu-id="60c73-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="60c73-115">Требования</span><span class="sxs-lookup"><span data-stu-id="60c73-115">Requirements</span></span>



| <span data-ttu-id="60c73-116">Требование</span><span class="sxs-lookup"><span data-stu-id="60c73-116">Requirement</span></span> | <span data-ttu-id="60c73-117">Значение</span><span class="sxs-lookup"><span data-stu-id="60c73-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60c73-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60c73-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60c73-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60c73-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="60c73-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60c73-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60c73-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60c73-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="60c73-122">Header</span><span class="sxs-lookup"><span data-stu-id="60c73-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60c73-123"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="60c73-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="60c73-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60c73-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="60c73-125"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60c73-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c73-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60c73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c73-127">**инсталлвиадевице**</span><span class="sxs-lookup"><span data-stu-id="60c73-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




