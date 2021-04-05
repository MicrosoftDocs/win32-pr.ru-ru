---
description: Функция Пдхвбжетонекаунтерпас отображает диалоговое окно, позволяющее пользователю просматривать доступные счетчики производительности и выбирать один счетчик.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: Функция Пдхвбжетонекаунтерпас
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909731"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="83e5a-103">Функция Пдхвбжетонекаунтерпас</span><span class="sxs-lookup"><span data-stu-id="83e5a-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="83e5a-104">Функция **пдхвбжетонекаунтерпас** отображает диалоговое окно, позволяющее пользователю просматривать доступные счетчики производительности и выбирать один счетчик.</span><span class="sxs-lookup"><span data-stu-id="83e5a-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="83e5a-105">Выбранный счетчик возвращается в переменной *PathString* .</span><span class="sxs-lookup"><span data-stu-id="83e5a-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="83e5a-106">Переменная *PathString* должна быть распределена и инициализирована перед вызовом этой функции, а размер измерения должен быть указан переменной *PathLength* .</span><span class="sxs-lookup"><span data-stu-id="83e5a-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83e5a-107">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="83e5a-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="83e5a-108">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="83e5a-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="83e5a-109">Функция Пдхвбжетонекаунтерпас ( \_ ByVal PathString в качестве строки, \_ ByVal PathLength как Long, ByVal \_ детаиллевел как Long, \_ ByVal каптионстринг как String \_ ) как long</span><span class="sxs-lookup"><span data-stu-id="83e5a-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="83e5a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="83e5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e5a-111">*PathString*</span><span class="sxs-lookup"><span data-stu-id="83e5a-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="83e5a-112">Инициализированная строковая переменная, используемая для получения пути счетчика, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="83e5a-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="83e5a-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="83e5a-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="83e5a-114">Длина инициализированного PathString.</span><span class="sxs-lookup"><span data-stu-id="83e5a-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="83e5a-115">*детаиллевел*</span><span class="sxs-lookup"><span data-stu-id="83e5a-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="83e5a-116">Типы счетчиков, отображаемых в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="83e5a-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="83e5a-117">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="83e5a-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="83e5a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="83e5a-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="83e5a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="83e5a-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="83e5a-120"><dt>**\_Дополнительные сведения о производительности \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83e5a-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="83e5a-121">Счетчики, которые могут быть понятны расширенному пользователю, а также счетчики новичков и пользователей.</span><span class="sxs-lookup"><span data-stu-id="83e5a-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="83e5a-122"><dt>**\_эксперт подробных сведений о производительности \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83e5a-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="83e5a-123">Счетчики, которые, скорее всего, будут понятны эксперту и разработчику программного обеспечения, а также счетчики для новичков и опытных пользователей.</span><span class="sxs-lookup"><span data-stu-id="83e5a-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="83e5a-124"><dt>**\_сведения о производительности — \_ новичок**</dt></span><span class="sxs-lookup"><span data-stu-id="83e5a-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="83e5a-125">Только счетчики, которые может понять пользователь новичка.</span><span class="sxs-lookup"><span data-stu-id="83e5a-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="83e5a-126"><dt>**\_Мастер сведений о производительности \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83e5a-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="83e5a-127">Все счетчики в системе.</span><span class="sxs-lookup"><span data-stu-id="83e5a-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="83e5a-128">*каптионстринг*</span><span class="sxs-lookup"><span data-stu-id="83e5a-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="83e5a-129">Строковая переменная, содержащая текст, который будет отображаться в строке заголовка диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="83e5a-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e5a-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83e5a-130">Return value</span></span>

<span data-ttu-id="83e5a-131">Функция возвращает число символов, записанных в буфер *PathString* .</span><span class="sxs-lookup"><span data-stu-id="83e5a-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e5a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="83e5a-132">Requirements</span></span>



| <span data-ttu-id="83e5a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="83e5a-133">Requirement</span></span> | <span data-ttu-id="83e5a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="83e5a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83e5a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83e5a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="83e5a-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83e5a-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83e5a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83e5a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="83e5a-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83e5a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83e5a-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83e5a-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="83e5a-140"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83e5a-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="83e5a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="83e5a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83e5a-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83e5a-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e5a-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83e5a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e5a-144">**пдхвбкреатекаунтерпаслист**</span><span class="sxs-lookup"><span data-stu-id="83e5a-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="83e5a-145">**пдхвбжеткаунтерпаселементс**</span><span class="sxs-lookup"><span data-stu-id="83e5a-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="83e5a-146">**пдхвбжеткаунтерпасфромлист**</span><span class="sxs-lookup"><span data-stu-id="83e5a-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




