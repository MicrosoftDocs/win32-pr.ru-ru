---
title: Макрос MCI_MAKE_HMS (МЦиапи. h)
description: '\_ \_ Макрос make ХМс создает значение времени в формате "Упакованные часы/минуты/секунды (ХМс)" из заданных значений часов, минут и секунд.'
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803508"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="5c2d5-104">\_Макрос make \_ ХМс</span><span class="sxs-lookup"><span data-stu-id="5c2d5-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="5c2d5-105">Макрос **\_ make \_ ХМс** создает значение времени в формате "Упакованные часы/минуты/секунды (ХМс)" из заданных значений часов, минут и секунд.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2d5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c2d5-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="5c2d5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c2d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2d5-108">*суток*</span><span class="sxs-lookup"><span data-stu-id="5c2d5-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2d5-109">Количество часов.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="5c2d5-110">*тезис*</span><span class="sxs-lookup"><span data-stu-id="5c2d5-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2d5-111">Количество минут.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="5c2d5-112">*секунд*</span><span class="sxs-lookup"><span data-stu-id="5c2d5-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2d5-113">Количество секунд.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2d5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c2d5-114">Return value</span></span>

<span data-ttu-id="5c2d5-115">Возвращает время в упакованном формате ХМС.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2d5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c2d5-116">Remarks</span></span>

<span data-ttu-id="5c2d5-117">Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="5c2d5-118">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-118">The most significant byte is unused.</span></span>

<span data-ttu-id="5c2d5-119">Макрос **\_ make \_ ХМс для MCI** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5c2d5-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="5c2d5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5c2d5-120">Requirements</span></span>



| <span data-ttu-id="5c2d5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5c2d5-121">Requirement</span></span> | <span data-ttu-id="5c2d5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5c2d5-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2d5-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c2d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2d5-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c2d5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5c2d5-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c2d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2d5-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c2d5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c2d5-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5c2d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2d5-128"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d5-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2d5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c2d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2d5-130">MCI</span><span class="sxs-lookup"><span data-stu-id="5c2d5-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5c2d5-131">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="5c2d5-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





