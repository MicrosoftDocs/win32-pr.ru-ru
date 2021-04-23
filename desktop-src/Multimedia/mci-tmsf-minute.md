---
title: Макрос MCI_TMSF_MINUTE (МЦиапи. h)
description: Макрос MCI \_ тмсф \_ Minute извлекает компонент минут из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- MCI_TMSF_MINUTE макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534202"
---
# <a name="mci_tmsf_minute-macro"></a><span data-ttu-id="41e6b-104">\_Макрос MCI тмсф \_ Minute</span><span class="sxs-lookup"><span data-stu-id="41e6b-104">MCI\_TMSF\_MINUTE macro</span></span>

<span data-ttu-id="41e6b-105">Макрос **MCI \_ тмсф \_ Minute** извлекает компонент минут из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).</span><span class="sxs-lookup"><span data-stu-id="41e6b-105">The **MCI\_TMSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e6b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41e6b-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_MINUTE(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="41e6b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="41e6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e6b-108">*двтмсф*</span><span class="sxs-lookup"><span data-stu-id="41e6b-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="41e6b-109">Время в формате ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="41e6b-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e6b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41e6b-110">Return value</span></span>

<span data-ttu-id="41e6b-111">Возвращает компонент минут указанной информации ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="41e6b-111">Returns the minutes component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e6b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41e6b-112">Remarks</span></span>

<span data-ttu-id="41e6b-113">Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.</span><span class="sxs-lookup"><span data-stu-id="41e6b-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="41e6b-114">Макрос **MCI \_ тмсф \_ Minute** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="41e6b-114">The **MCI\_TMSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="41e6b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="41e6b-115">Requirements</span></span>



| <span data-ttu-id="41e6b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="41e6b-116">Requirement</span></span> | <span data-ttu-id="41e6b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="41e6b-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41e6b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41e6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="41e6b-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41e6b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41e6b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41e6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="41e6b-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41e6b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41e6b-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41e6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e6b-123"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="41e6b-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e6b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41e6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e6b-125">MCI</span><span class="sxs-lookup"><span data-stu-id="41e6b-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="41e6b-126">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="41e6b-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





