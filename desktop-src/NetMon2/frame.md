---
description: Фактический кадр из драйвера.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Структура ФРЕЙМа (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673195"
---
# <a name="frame-structure"></a><span data-ttu-id="c3a8c-103">Структура ФРЕЙМа</span><span class="sxs-lookup"><span data-stu-id="c3a8c-103">FRAME structure</span></span>

<span data-ttu-id="c3a8c-104">Структура **фрейма** — это фактический кадр из драйвера.</span><span class="sxs-lookup"><span data-stu-id="c3a8c-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3a8c-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="c3a8c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c3a8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3a8c-107">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="c3a8c-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="c3a8c-108">Затраченное время (в микросекундах) между началом записи и временем записи кадра.</span><span class="sxs-lookup"><span data-stu-id="c3a8c-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="c3a8c-109">**фрамеленгс**</span><span class="sxs-lookup"><span data-stu-id="c3a8c-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="c3a8c-110">Длина фрейма MAC.</span><span class="sxs-lookup"><span data-stu-id="c3a8c-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="c3a8c-111">**нбитесаваил**</span><span class="sxs-lookup"><span data-stu-id="c3a8c-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="c3a8c-112">Фактическая длина кадра скопирована.</span><span class="sxs-lookup"><span data-stu-id="c3a8c-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="c3a8c-113">**макфраме**</span><span class="sxs-lookup"><span data-stu-id="c3a8c-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="c3a8c-114">Данные кадра.</span><span class="sxs-lookup"><span data-stu-id="c3a8c-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3a8c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c3a8c-115">Requirements</span></span>



| <span data-ttu-id="c3a8c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c3a8c-116">Requirement</span></span> | <span data-ttu-id="c3a8c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c3a8c-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a8c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3a8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a8c-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3a8c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c3a8c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3a8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a8c-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3a8c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c3a8c-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c3a8c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3a8c-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a8c-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




