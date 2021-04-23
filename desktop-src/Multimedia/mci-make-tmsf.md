---
title: Макрос MCI_MAKE_TMSF (МЦиапи. h)
description: '\_ \_ Макрос make тмсф создает значение времени в упакованном формате дорожек/минут/секунд/кадров (тмсф) из заданных дорожек, минут, секунд и значений кадров.'
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672890"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="cdace-104">\_Макрос make \_ тмсф</span><span class="sxs-lookup"><span data-stu-id="cdace-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="cdace-105">Макрос **\_ make \_ тмсф** создает значение времени в упакованном формате дорожек/минут/секунд/кадров (тмсф) из заданных дорожек, минут, секунд и значений кадров.</span><span class="sxs-lookup"><span data-stu-id="cdace-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdace-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdace-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="cdace-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdace-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdace-108">*tracks*</span><span class="sxs-lookup"><span data-stu-id="cdace-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="cdace-109">Число дорожек.</span><span class="sxs-lookup"><span data-stu-id="cdace-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="cdace-110">*тезис*</span><span class="sxs-lookup"><span data-stu-id="cdace-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="cdace-111">Количество минут.</span><span class="sxs-lookup"><span data-stu-id="cdace-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="cdace-112">*секунд*</span><span class="sxs-lookup"><span data-stu-id="cdace-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="cdace-113">Количество секунд.</span><span class="sxs-lookup"><span data-stu-id="cdace-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="cdace-114">*рамки*</span><span class="sxs-lookup"><span data-stu-id="cdace-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="cdace-115">Число кадров.</span><span class="sxs-lookup"><span data-stu-id="cdace-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdace-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdace-116">Return value</span></span>

<span data-ttu-id="cdace-117">Возвращает время в упакованном формате ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="cdace-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdace-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdace-118">Remarks</span></span>

<span data-ttu-id="cdace-119">Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.</span><span class="sxs-lookup"><span data-stu-id="cdace-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="cdace-120">Макрос **\_ make \_ тмсф для MCI** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cdace-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="cdace-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cdace-121">Requirements</span></span>



| <span data-ttu-id="cdace-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cdace-122">Requirement</span></span> | <span data-ttu-id="cdace-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cdace-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cdace-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdace-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cdace-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdace-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cdace-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdace-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cdace-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cdace-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cdace-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cdace-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdace-129"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdace-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdace-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdace-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdace-131">MCI</span><span class="sxs-lookup"><span data-stu-id="cdace-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cdace-132">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="cdace-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





