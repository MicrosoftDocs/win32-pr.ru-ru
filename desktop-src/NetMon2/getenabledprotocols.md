---
description: Функция Жетенабледпротоколс возвращает таблицу всех протоколов, помеченных как включенные.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Функция Жетенабледпротоколс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650480"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="b4564-103">Функция Жетенабледпротоколс</span><span class="sxs-lookup"><span data-stu-id="b4564-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="b4564-104">Функция **жетенабледпротоколс** возвращает таблицу всех протоколов, помеченных как включенные.</span><span class="sxs-lookup"><span data-stu-id="b4564-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4564-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4564-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="b4564-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4564-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4564-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4564-108">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="b4564-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4564-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4564-109">Return value</span></span>

<span data-ttu-id="b4564-110">Если функция выполнена успешно, возвращаемое значение является указателем на структуру [протоколтабле](protocoltable.md) , в которой перечислены все включенные протоколы в записи.</span><span class="sxs-lookup"><span data-stu-id="b4564-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="b4564-111">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="b4564-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4564-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4564-112">Remarks</span></span>

<span data-ttu-id="b4564-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетенабледпротоколс** .</span><span class="sxs-lookup"><span data-stu-id="b4564-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4564-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b4564-114">Requirements</span></span>



| <span data-ttu-id="b4564-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b4564-115">Requirement</span></span> | <span data-ttu-id="b4564-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b4564-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4564-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4564-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4564-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4564-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b4564-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4564-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4564-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4564-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b4564-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b4564-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4564-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4564-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b4564-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4564-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4564-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4564-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4564-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4564-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4564-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4564-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4564-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4564-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4564-128">протоколтабле</span><span class="sxs-lookup"><span data-stu-id="b4564-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 




