---
title: Макрос MCI_TMSF_TRACK (МЦиапи. h)
description: Макрос MCI \_ тмсф \_ Track извлекает компонент треки из параметра, содержащего сведения о упакованных дорожках/минутах/сек/Frames (тмсф).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892049"
---
# <a name="mci_tmsf_track-macro"></a><span data-ttu-id="1ec35-104">\_Макрос MCI тмсф \_ Track</span><span class="sxs-lookup"><span data-stu-id="1ec35-104">MCI\_TMSF\_TRACK macro</span></span>

<span data-ttu-id="1ec35-105">Макрос **MCI \_ тмсф \_ Track** извлекает компонент треки из параметра, содержащего сведения о упакованных дорожках/минутах/сек/Frames (тмсф).</span><span class="sxs-lookup"><span data-stu-id="1ec35-105">The **MCI\_TMSF\_TRACK** macro retrieves the tracks component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec35-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec35-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="1ec35-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec35-108">*двтмсф*</span><span class="sxs-lookup"><span data-stu-id="1ec35-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec35-109">Время в формате ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="1ec35-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec35-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec35-110">Return value</span></span>

<span data-ttu-id="1ec35-111">Возвращает компонент дорожек указанной информации ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="1ec35-111">Returns the tracks component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec35-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ec35-112">Remarks</span></span>

<span data-ttu-id="1ec35-113">Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.</span><span class="sxs-lookup"><span data-stu-id="1ec35-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="1ec35-114">Макрос **MCI \_ тмсф \_ Track** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1ec35-114">The **MCI\_TMSF\_TRACK** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a><span data-ttu-id="1ec35-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec35-115">Requirements</span></span>



| <span data-ttu-id="1ec35-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec35-116">Requirement</span></span> | <span data-ttu-id="1ec35-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec35-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec35-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ec35-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec35-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1ec35-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1ec35-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ec35-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec35-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1ec35-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ec35-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1ec35-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec35-123"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec35-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec35-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ec35-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec35-125">MCI</span><span class="sxs-lookup"><span data-stu-id="1ec35-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1ec35-126">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="1ec35-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





