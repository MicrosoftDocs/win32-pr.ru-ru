---
description: Находит следующий кадр в текущем контексте записи, соответствующий фильтру.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Функция Финднекстфраме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540226"
---
# <a name="findnextframe-function"></a><span data-ttu-id="b6214-103">Функция Финднекстфраме</span><span class="sxs-lookup"><span data-stu-id="b6214-103">FindNextFrame function</span></span>

<span data-ttu-id="b6214-104">Функция **финднекстфраме** находит следующий кадр в текущем контексте отслеживания, соответствующий фильтру.</span><span class="sxs-lookup"><span data-stu-id="b6214-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6214-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6214-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="b6214-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6214-107">*хкуррентфраме*</span><span class="sxs-lookup"><span data-stu-id="b6214-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-108">Маркер фрейма.</span><span class="sxs-lookup"><span data-stu-id="b6214-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b6214-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="b6214-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-110">Имя протокола, например TCP.</span><span class="sxs-lookup"><span data-stu-id="b6214-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="b6214-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="b6214-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-112">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="b6214-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="b6214-113">*саурцеаддресс*</span><span class="sxs-lookup"><span data-stu-id="b6214-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-114">Исходный адрес.</span><span class="sxs-lookup"><span data-stu-id="b6214-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="b6214-115">*протоколоффсет*</span><span class="sxs-lookup"><span data-stu-id="b6214-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-116">Указатель на **слово** , которое будет принимать смещение протокола.</span><span class="sxs-lookup"><span data-stu-id="b6214-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="b6214-117">*оригиналфраменумбер*</span><span class="sxs-lookup"><span data-stu-id="b6214-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-118">Начальная точка поиска.</span><span class="sxs-lookup"><span data-stu-id="b6214-118">The starting point of the search.</span></span> <span data-ttu-id="b6214-119">По умолчанию эта функция выполняет поиск в пересылках кадров 1 000, начиная с начальной точки *оригиналфраменумбер* .</span><span class="sxs-lookup"><span data-stu-id="b6214-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="b6214-120">Чтобы изменить расстояние поиска вперед, добавьте эту строку в файл Nmapi.ini, расположенный в \\ каталоге сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="b6214-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="b6214-121">МАКСЛУКБАКК =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="b6214-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="b6214-122">*хигхестфраме*</span><span class="sxs-lookup"><span data-stu-id="b6214-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b6214-123">Наибольший номер кадра в записи, в которой выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="b6214-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6214-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6214-124">Return value</span></span>

<span data-ttu-id="b6214-125">Если функция выполнена успешно, возвращаемое значение является маркером для следующего кадра.</span><span class="sxs-lookup"><span data-stu-id="b6214-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="b6214-126">Если функция не выполнена успешно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="b6214-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6214-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6214-127">Remarks</span></span>

<span data-ttu-id="b6214-128">Фильтр записи определяется в первую очередь параметром *ProtocolName* , который является единственным обязательным входом фильтра. Вы можете добавить данные *дестинатионаддресс* и *саурцеаддресс* , чтобы увеличить скорость записи.</span><span class="sxs-lookup"><span data-stu-id="b6214-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="b6214-129">Указатель *протоколоффсет* возвращается вызывающему средству синтаксического анализа, который добавляет **слово** к указателю, возвращаемому при блокировке кадра (WITH [Парсертемпорарилоккфраме](parsertemporarylockframe.md)), чтобы получить **LPBYTE** протокола для поиска.</span><span class="sxs-lookup"><span data-stu-id="b6214-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="b6214-130">При возврате ХФРАМЕ, которому был передан фильтр, выдается анализатору.</span><span class="sxs-lookup"><span data-stu-id="b6214-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="b6214-131">Если средство синтаксического анализа обнаруживает, что этот кадр не найден, средство синтаксического анализа может передать ХФРАМЕ обратно в функцию **финднекстфраме** , чтобы получить следующий кадр.</span><span class="sxs-lookup"><span data-stu-id="b6214-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="b6214-132">Исходный и конечный адреса не являются обязательными и могут быть переданы как **null**.</span><span class="sxs-lookup"><span data-stu-id="b6214-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6214-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b6214-133">Requirements</span></span>



| <span data-ttu-id="b6214-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b6214-134">Requirement</span></span> | <span data-ttu-id="b6214-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b6214-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6214-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6214-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b6214-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6214-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b6214-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6214-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b6214-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6214-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6214-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6214-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6214-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6214-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b6214-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6214-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6214-143"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6214-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6214-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b6214-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6214-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6214-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




