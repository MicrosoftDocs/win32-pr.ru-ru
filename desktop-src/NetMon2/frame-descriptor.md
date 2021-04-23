---
description: '\_Структура дескрипторов кадров предоставляет описательные сведения о необработанных кадрах.'
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Структура FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673197"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="e32aa-103">\_Структура дескриптора кадра</span><span class="sxs-lookup"><span data-stu-id="e32aa-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="e32aa-104">Структура **\_ дескрипторов кадров** предоставляет описательные сведения о необработанных кадрах.</span><span class="sxs-lookup"><span data-stu-id="e32aa-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e32aa-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="e32aa-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e32aa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e32aa-107">**фрамепоинтер**</span><span class="sxs-lookup"><span data-stu-id="e32aa-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-108">Указатель на данные кадра.</span><span class="sxs-lookup"><span data-stu-id="e32aa-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-109">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="e32aa-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-110">Системное время в микросекундах при записи кадра.</span><span class="sxs-lookup"><span data-stu-id="e32aa-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="e32aa-111">Это время обычно используется для определения интервала между временем записи двух кадров.</span><span class="sxs-lookup"><span data-stu-id="e32aa-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-112">**фрамеленгс**</span><span class="sxs-lookup"><span data-stu-id="e32aa-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-113">Длина кадра.</span><span class="sxs-lookup"><span data-stu-id="e32aa-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-114">**нбитесаваил**</span><span class="sxs-lookup"><span data-stu-id="e32aa-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-115">Фактическая длина кадра скопирована.</span><span class="sxs-lookup"><span data-stu-id="e32aa-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-116">**ETYPE**</span><span class="sxs-lookup"><span data-stu-id="e32aa-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-117">Имя etype.</span><span class="sxs-lookup"><span data-stu-id="e32aa-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-118">**Протокола**</span><span class="sxs-lookup"><span data-stu-id="e32aa-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-119">Значение SAP.</span><span class="sxs-lookup"><span data-stu-id="e32aa-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-120">**ловпротокол**</span><span class="sxs-lookup"><span data-stu-id="e32aa-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-121">Индекс найденного протокола.</span><span class="sxs-lookup"><span data-stu-id="e32aa-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-122">**ловпротоколоффсет**</span><span class="sxs-lookup"><span data-stu-id="e32aa-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-123">Смещение к данным протокола, полученным от **ловпротокол**.</span><span class="sxs-lookup"><span data-stu-id="e32aa-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-124">**хигхпорт**</span><span class="sxs-lookup"><span data-stu-id="e32aa-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-125">Порт высокого протокола, определенный в **ловпротокол**.</span><span class="sxs-lookup"><span data-stu-id="e32aa-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="e32aa-126">**хигхпротоколоффсет**</span><span class="sxs-lookup"><span data-stu-id="e32aa-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e32aa-127">Смещение к данным протокола, полученным от **хигхпорт**.</span><span class="sxs-lookup"><span data-stu-id="e32aa-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e32aa-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e32aa-128">Requirements</span></span>



| <span data-ttu-id="e32aa-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e32aa-129">Requirement</span></span> | <span data-ttu-id="e32aa-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e32aa-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e32aa-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e32aa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e32aa-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e32aa-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e32aa-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e32aa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e32aa-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e32aa-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e32aa-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e32aa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e32aa-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e32aa-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




