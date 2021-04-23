---
description: Функция Финдпревиаусфраме находит предыдущий кадр в текущем контексте записи, соответствующий фильтру.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Функция Финдпревиаусфраме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990912"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="83765-103">Функция Финдпревиаусфраме</span><span class="sxs-lookup"><span data-stu-id="83765-103">FindPreviousFrame function</span></span>

<span data-ttu-id="83765-104">Функция **финдпревиаусфраме** находит предыдущий кадр в текущем контексте записи, соответствующий фильтру.</span><span class="sxs-lookup"><span data-stu-id="83765-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="83765-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83765-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="83765-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83765-107">*хкуррентфраме*</span><span class="sxs-lookup"><span data-stu-id="83765-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="83765-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="83765-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="83765-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-110">Имя протокола, например TCP.</span><span class="sxs-lookup"><span data-stu-id="83765-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="83765-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="83765-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-112">Адрес назначения кадра, поиск которого выполняется.</span><span class="sxs-lookup"><span data-stu-id="83765-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="83765-113">*саурцеаддресс*</span><span class="sxs-lookup"><span data-stu-id="83765-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-114">Исходный адрес кадра, поиск которого выполняется.</span><span class="sxs-lookup"><span data-stu-id="83765-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="83765-115">*протоколоффсет*</span><span class="sxs-lookup"><span data-stu-id="83765-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-116">Указатель на **слово** , получающее смещение протокола.</span><span class="sxs-lookup"><span data-stu-id="83765-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="83765-117">*оригиналфраменумбер*</span><span class="sxs-lookup"><span data-stu-id="83765-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-118">Начальная точка поиска.</span><span class="sxs-lookup"><span data-stu-id="83765-118">Starting point of the search.</span></span> <span data-ttu-id="83765-119">По умолчанию эта функция ищет в обратном направлении 1 000 кадров от начальной точки *оригиналфраменумбер* .</span><span class="sxs-lookup"><span data-stu-id="83765-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="83765-120">Можно изменить расстояние поиска обратно, добавив эту строку в файл Nmapi.ini, который находится в \\ каталоге сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="83765-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="83765-121">МАКСЛУКБАКК =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="83765-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="83765-122">*ловестфраме*</span><span class="sxs-lookup"><span data-stu-id="83765-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="83765-123">Наименьший номер кадра в записи, в которой выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="83765-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83765-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83765-124">Return value</span></span>

<span data-ttu-id="83765-125">Если функция выполнена успешно, возвращаемое значение является обработчиком предыдущего кадра.</span><span class="sxs-lookup"><span data-stu-id="83765-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="83765-126">Если функция не выполнена успешно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="83765-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="83765-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83765-127">Remarks</span></span>

<span data-ttu-id="83765-128">Фильтр записи определяется главным образом *ProtocolName*, который является единственным необходимым входным фильтром. Вы можете добавить сведения *дестинатионаддресс* и *саурцеаддресс* , чтобы увеличить скорость записи.</span><span class="sxs-lookup"><span data-stu-id="83765-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="83765-129">*Протоколоффсет* возвращается вызывающему средству синтаксического анализа, который добавляет этот **DWORD** в указатель, возвращаемый, заблокируя кадр (WITH [ПАРСЕРТЕМПОРАРИЛОККФРАМЕ](parsertemporarylockframe.md)), чтобы получить LPBYTE протокола, для которого выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="83765-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="83765-130">При возврате ХФРАМЕ, которому был передан фильтр, выдается анализатору.</span><span class="sxs-lookup"><span data-stu-id="83765-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="83765-131">Если средство синтаксического анализа обнаруживает, что кадр не найден, средство синтаксического анализа может передать этот ХФРАМЕ обратно в функцию **финдпревиаусфраме** , чтобы получить следующий кадр.</span><span class="sxs-lookup"><span data-stu-id="83765-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="83765-132">Адреса источника и назначения, которые не являются обязательными, могут быть переданы как **null**.</span><span class="sxs-lookup"><span data-stu-id="83765-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="83765-133">При использовании эти адреса могут иметь тип \_ \_ IP-адреса и т. д., а не только типы Mac.</span><span class="sxs-lookup"><span data-stu-id="83765-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="83765-134">Требования</span><span class="sxs-lookup"><span data-stu-id="83765-134">Requirements</span></span>



| <span data-ttu-id="83765-135">Требование</span><span class="sxs-lookup"><span data-stu-id="83765-135">Requirement</span></span> | <span data-ttu-id="83765-136">Значение</span><span class="sxs-lookup"><span data-stu-id="83765-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="83765-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83765-137">Minimum supported client</span></span><br/> | <span data-ttu-id="83765-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83765-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="83765-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83765-139">Minimum supported server</span></span><br/> | <span data-ttu-id="83765-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83765-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="83765-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="83765-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="83765-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="83765-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="83765-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83765-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="83765-144"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83765-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="83765-145">DLL</span><span class="sxs-lookup"><span data-stu-id="83765-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83765-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83765-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




