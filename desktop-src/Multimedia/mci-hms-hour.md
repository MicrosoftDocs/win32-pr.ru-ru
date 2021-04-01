---
title: Макрос MCI_HMS_HOUR (МЦиапи. h)
description: Макрос MCI \_ ХМс \_ Hour извлекает компонент часов из параметра, содержащего сведения о упакованных часах/минутах/секундах (ХМс).
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072003"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="f22f3-104">\_Макрос MCI ХМс \_ часа</span><span class="sxs-lookup"><span data-stu-id="f22f3-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="f22f3-105">Макрос **MCI \_ ХМс \_ Hour** извлекает компонент часов из параметра, содержащего сведения о упакованных часах/минутах/секундах (ХМс).</span><span class="sxs-lookup"><span data-stu-id="f22f3-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22f3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f22f3-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="f22f3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f22f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f22f3-108">*двхмс*</span><span class="sxs-lookup"><span data-stu-id="f22f3-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="f22f3-109">Время в формате ХМС.</span><span class="sxs-lookup"><span data-stu-id="f22f3-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f22f3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f22f3-110">Return value</span></span>

<span data-ttu-id="f22f3-111">Возвращает компонент часов указанной информации ХМС.</span><span class="sxs-lookup"><span data-stu-id="f22f3-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="f22f3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f22f3-112">Remarks</span></span>

<span data-ttu-id="f22f3-113">Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды.</span><span class="sxs-lookup"><span data-stu-id="f22f3-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="f22f3-114">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="f22f3-114">The most significant byte is unused.</span></span>

<span data-ttu-id="f22f3-115">Макрос **MCI \_ ХМс \_ Hour** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f22f3-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="f22f3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f22f3-116">Requirements</span></span>



| <span data-ttu-id="f22f3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f22f3-117">Requirement</span></span> | <span data-ttu-id="f22f3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f22f3-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f22f3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f22f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f22f3-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f22f3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f22f3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f22f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f22f3-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f22f3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f22f3-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f22f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f22f3-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f22f3-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22f3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f22f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22f3-126">MCI</span><span class="sxs-lookup"><span data-stu-id="f22f3-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f22f3-127">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="f22f3-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





