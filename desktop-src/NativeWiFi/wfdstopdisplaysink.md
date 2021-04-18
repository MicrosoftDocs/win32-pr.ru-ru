---
description: Останавливает режим приемника Miracast, отключает возможность обнаружения и отменяет регистрацию обратного вызова.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Функция Вфддисплайсинкстоп (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673491"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="b8761-103">Функция Вфддисплайсинкстоп</span><span class="sxs-lookup"><span data-stu-id="b8761-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="b8761-104">Останавливает режим приемника Miracast, отключает возможность обнаружения и отменяет регистрацию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b8761-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="b8761-105">Приложение должно вызывать это после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="b8761-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8761-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8761-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="b8761-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8761-107">Parameters</span></span>

<span data-ttu-id="b8761-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="b8761-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8761-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8761-109">Return value</span></span>

<span data-ttu-id="b8761-110">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b8761-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8761-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8761-111">Remarks</span></span>

<span data-ttu-id="b8761-112">Ожидается, что приложение разблокировало все выполняемые обратные вызовы перед вызовом **вфдстопдисплайсинк**.</span><span class="sxs-lookup"><span data-stu-id="b8761-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8761-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b8761-113">Requirements</span></span>



| <span data-ttu-id="b8761-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b8761-114">Requirement</span></span> | <span data-ttu-id="b8761-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b8761-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8761-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8761-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8761-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8761-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b8761-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8761-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8761-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8761-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8761-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b8761-120">End of client support</span></span><br/>    | <span data-ttu-id="b8761-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b8761-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="b8761-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b8761-122">End of server support</span></span><br/>    | <span data-ttu-id="b8761-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8761-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="b8761-124">Header</span><span class="sxs-lookup"><span data-stu-id="b8761-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8761-125"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8761-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="b8761-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8761-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8761-127"><dt>Вифидисплай. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8761-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8761-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b8761-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8761-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8761-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




