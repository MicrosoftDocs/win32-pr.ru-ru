---
title: Макрос MCI_MAKE_MSF (МЦиапи. h)
description: С помощью \_ MCI \_ макрос MSF создает значение времени в формате упакованных минут/секунд/кадров (MSF) с учетом заданных минут, секунд и значений кадров.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989348"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="246dd-104">MCI \_ делает \_ макрос MSF</span><span class="sxs-lookup"><span data-stu-id="246dd-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="246dd-105">С помощью **MCI макрос \_ \_ MSF** создает значение времени в формате упакованных минут/секунд/кадров (MSF) с учетом заданных минут, секунд и значений кадров.</span><span class="sxs-lookup"><span data-stu-id="246dd-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="246dd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="246dd-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="246dd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="246dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="246dd-108">*тезис*</span><span class="sxs-lookup"><span data-stu-id="246dd-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="246dd-109">Количество минут.</span><span class="sxs-lookup"><span data-stu-id="246dd-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="246dd-110">*секунд*</span><span class="sxs-lookup"><span data-stu-id="246dd-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="246dd-111">Количество секунд.</span><span class="sxs-lookup"><span data-stu-id="246dd-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="246dd-112">*рамки*</span><span class="sxs-lookup"><span data-stu-id="246dd-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="246dd-113">Число кадров.</span><span class="sxs-lookup"><span data-stu-id="246dd-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="246dd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="246dd-114">Return value</span></span>

<span data-ttu-id="246dd-115">Возвращает время в упакованном формате MSF.</span><span class="sxs-lookup"><span data-stu-id="246dd-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="246dd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="246dd-116">Remarks</span></span>

<span data-ttu-id="246dd-117">Время в формате MSF выражается в виде значения **типа DWORD** с наименьшим значащим байтом, содержащим минуты, следующим наименее значащим байтом, содержащим секунды, и следующим наименьшим значащим байтом, содержащим кадры.</span><span class="sxs-lookup"><span data-stu-id="246dd-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="246dd-118">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="246dd-118">The most significant byte is unused.</span></span>

<span data-ttu-id="246dd-119">Элемент **MCI \_ делает макрос \_ MSF** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="246dd-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="246dd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="246dd-120">Requirements</span></span>



| <span data-ttu-id="246dd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="246dd-121">Requirement</span></span> | <span data-ttu-id="246dd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="246dd-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="246dd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="246dd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="246dd-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="246dd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="246dd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="246dd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="246dd-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="246dd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="246dd-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="246dd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="246dd-128"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="246dd-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="246dd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="246dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246dd-130">MCI</span><span class="sxs-lookup"><span data-stu-id="246dd-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="246dd-131">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="246dd-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





