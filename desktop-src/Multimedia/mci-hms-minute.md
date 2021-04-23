---
title: Макрос MCI_HMS_MINUTE (МЦиапи. h)
description: Макрос MCI \_ ХМс \_ Minute извлекает компонент минут из параметра, содержащего Упакованные данные о часах/минутах/секундах (ХМс).
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137586"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="8a2c6-104">\_Макрос MCI ХМс \_ Minute</span><span class="sxs-lookup"><span data-stu-id="8a2c6-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="8a2c6-105">Макрос **MCI \_ ХМс \_ Minute** извлекает компонент минут из параметра, содержащего Упакованные данные о часах/минутах/секундах (ХМс).</span><span class="sxs-lookup"><span data-stu-id="8a2c6-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2c6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a2c6-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="8a2c6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a2c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2c6-108">*двхмс*</span><span class="sxs-lookup"><span data-stu-id="8a2c6-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="8a2c6-109">Время в формате ХМС.</span><span class="sxs-lookup"><span data-stu-id="8a2c6-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2c6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a2c6-110">Return value</span></span>

<span data-ttu-id="8a2c6-111">Возвращает компонент минут указанной информации ХМС.</span><span class="sxs-lookup"><span data-stu-id="8a2c6-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a2c6-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a2c6-112">Remarks</span></span>

<span data-ttu-id="8a2c6-113">Время в формате ХМС выражается как значение **DWORD** с наименьшим значащим байтом, содержащим часы, следующий младший значащий байт, содержащий минуты, и следующий младший значащий байт, содержащий секунды.</span><span class="sxs-lookup"><span data-stu-id="8a2c6-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="8a2c6-114">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="8a2c6-114">The most significant byte is unused.</span></span>

<span data-ttu-id="8a2c6-115">Макрос **MCI \_ ХМс \_ Minute** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8a2c6-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="8a2c6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8a2c6-116">Requirements</span></span>



| <span data-ttu-id="8a2c6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8a2c6-117">Requirement</span></span> | <span data-ttu-id="8a2c6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8a2c6-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2c6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a2c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2c6-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a2c6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8a2c6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a2c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2c6-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a2c6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8a2c6-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8a2c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a2c6-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a2c6-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a2c6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a2c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2c6-126">MCI</span><span class="sxs-lookup"><span data-stu-id="8a2c6-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8a2c6-127">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="8a2c6-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





