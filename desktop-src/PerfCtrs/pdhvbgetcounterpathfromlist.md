---
description: Функция Пдхвбжеткаунтерпасфромлист копирует путь счетчика, на который ссылается параметр index, из списка путей счетчиков, созданного пользователем, из последнего вызова функции Пдхвбкреатекаунтерпаслист.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Функция Пдхвбжеткаунтерпасфромлист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663217"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="83672-103">Функция Пдхвбжеткаунтерпасфромлист</span><span class="sxs-lookup"><span data-stu-id="83672-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="83672-104">Функция **пдхвбжеткаунтерпасфромлист** копирует путь счетчика, на который ссылается параметр *index* , из списка путей счетчиков, созданного пользователем, из последнего вызова функции [**пдхвбкреатекаунтерпаслист**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="83672-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83672-105">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="83672-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="83672-106">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="83672-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="83672-107">Функция Пдхвбжеткаунтерпасфромлист ( \_ ByVal индекс как Long, \_ буфер ByVal как строка, \_ ByVal BufferLength как long \_ ) как long</span><span class="sxs-lookup"><span data-stu-id="83672-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="83672-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83672-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83672-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="83672-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="83672-110">Индекс извлекаемого пути к счетчику.</span><span class="sxs-lookup"><span data-stu-id="83672-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="83672-111">Это должно быть значение, большее или равное 1 и меньшее или равное значению, возвращенному функцией [**пдхвбкреатекаунтерпаслист**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="83672-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="83672-112">*Буфер*</span><span class="sxs-lookup"><span data-stu-id="83672-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="83672-113">Измеренная и Инициализированная строка, которая получит путь к счетчику, соответствующий значению параметра индекса.</span><span class="sxs-lookup"><span data-stu-id="83672-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="83672-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="83672-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="83672-115">Максимальное число символов, которые будут помещаться в строку, на которую ссылается buffer.</span><span class="sxs-lookup"><span data-stu-id="83672-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83672-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83672-116">Return value</span></span>

<span data-ttu-id="83672-117">Функция возвращает число символов, скопированных в буфер.</span><span class="sxs-lookup"><span data-stu-id="83672-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="83672-118">Требования</span><span class="sxs-lookup"><span data-stu-id="83672-118">Requirements</span></span>



| <span data-ttu-id="83672-119">Требование</span><span class="sxs-lookup"><span data-stu-id="83672-119">Requirement</span></span> | <span data-ttu-id="83672-120">Значение</span><span class="sxs-lookup"><span data-stu-id="83672-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83672-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83672-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83672-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83672-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83672-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83672-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83672-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83672-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83672-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83672-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="83672-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83672-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="83672-127">DLL</span><span class="sxs-lookup"><span data-stu-id="83672-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83672-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83672-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83672-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83672-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83672-130">**пдхвбкреатекаунтерпаслист**</span><span class="sxs-lookup"><span data-stu-id="83672-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="83672-131">**пдхвбжеткаунтерпаселементс**</span><span class="sxs-lookup"><span data-stu-id="83672-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="83672-132">**пдхвбжетонекаунтерпас**</span><span class="sxs-lookup"><span data-stu-id="83672-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




