---
title: Макрос MCI_TMSF_FRAME (МЦиапи. h)
description: '\_Макрос ТМСФ MCI \_ получает компонент frames из параметра, содержащего данные упакованных дорожек/минут/секунд/кадров (тмсф).'
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801342"
---
# <a name="mci_tmsf_frame-macro"></a><span data-ttu-id="b4b68-104">\_Макрос ТМСФ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b4b68-104">MCI\_TMSF\_FRAME macro</span></span>

<span data-ttu-id="b4b68-105">Макрос **\_ тмсф MCI \_** получает компонент frames из параметра, содержащего данные упакованных дорожек/минут/секунд/кадров (тмсф).</span><span class="sxs-lookup"><span data-stu-id="b4b68-105">The **MCI\_TMSF\_FRAME** macro retrieves the frames component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b68-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4b68-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="b4b68-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4b68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b68-108">*двтмсф*</span><span class="sxs-lookup"><span data-stu-id="b4b68-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="b4b68-109">Время в формате ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="b4b68-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b68-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4b68-110">Return value</span></span>

<span data-ttu-id="b4b68-111">Возвращает компонент frames указанной ТМСФ информации.</span><span class="sxs-lookup"><span data-stu-id="b4b68-111">Returns the frames component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b68-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4b68-112">Remarks</span></span>

<span data-ttu-id="b4b68-113">Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.</span><span class="sxs-lookup"><span data-stu-id="b4b68-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="b4b68-114">Макрос **\_ \_ тмсф MCI** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4b68-114">The **MCI\_TMSF\_FRAME** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a><span data-ttu-id="b4b68-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b4b68-115">Requirements</span></span>



| <span data-ttu-id="b4b68-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b4b68-116">Requirement</span></span> | <span data-ttu-id="b4b68-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b4b68-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b68-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4b68-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b68-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4b68-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b4b68-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4b68-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b68-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4b68-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b4b68-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b4b68-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b68-123"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b68-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b68-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4b68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b68-125">MCI</span><span class="sxs-lookup"><span data-stu-id="b4b68-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b4b68-126">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="b4b68-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





