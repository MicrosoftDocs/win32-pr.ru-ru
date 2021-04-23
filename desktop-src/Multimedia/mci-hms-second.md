---
title: Макрос MCI_HMS_SECOND (МЦиапи. h)
description: '\_ \_ Второй макрос MCI ХМс извлекает компонент секунд из параметра, содержащего Упакованные данные о часах/минутах/секундах (ХМс).'
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892682"
---
# <a name="mci_hms_second-macro"></a><span data-ttu-id="5242b-104">\_ \_ Второй макрос MCI ХМс</span><span class="sxs-lookup"><span data-stu-id="5242b-104">MCI\_HMS\_SECOND macro</span></span>

<span data-ttu-id="5242b-105">**\_ \_ Второй макрос MCI ХМс** извлекает компонент секунд из параметра, содержащего Упакованные данные о часах/минутах/секундах (ХМс).</span><span class="sxs-lookup"><span data-stu-id="5242b-105">The **MCI\_HMS\_SECOND** macro retrieves the seconds component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5242b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5242b-106">Syntax</span></span>


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="5242b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5242b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5242b-108">*двхмс*</span><span class="sxs-lookup"><span data-stu-id="5242b-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="5242b-109">Время в формате ХМС.</span><span class="sxs-lookup"><span data-stu-id="5242b-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5242b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5242b-110">Return value</span></span>

<span data-ttu-id="5242b-111">Возвращает компонент секунд указанной информации ХМС.</span><span class="sxs-lookup"><span data-stu-id="5242b-111">Returns the seconds component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="5242b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5242b-112">Remarks</span></span>

<span data-ttu-id="5242b-113">Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды.</span><span class="sxs-lookup"><span data-stu-id="5242b-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="5242b-114">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="5242b-114">The most significant byte is unused.</span></span>

<span data-ttu-id="5242b-115">**Второй макрос \_ ХМс \_ MCI** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5242b-115">The **MCI\_HMS\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="5242b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5242b-116">Requirements</span></span>



| <span data-ttu-id="5242b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5242b-117">Requirement</span></span> | <span data-ttu-id="5242b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5242b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5242b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5242b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5242b-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5242b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5242b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5242b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5242b-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5242b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5242b-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5242b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5242b-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5242b-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5242b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5242b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5242b-126">MCI</span><span class="sxs-lookup"><span data-stu-id="5242b-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5242b-127">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="5242b-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





