---
title: Макрос MCI_TMSF_SECOND (МЦиапи. h)
description: '\_ \_ Второй макрос MCI тмсф извлекает компонент секунд из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).'
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136118"
---
# <a name="mci_tmsf_second-macro"></a><span data-ttu-id="28fa3-104">\_ \_ Второй макрос MCI тмсф</span><span class="sxs-lookup"><span data-stu-id="28fa3-104">MCI\_TMSF\_SECOND macro</span></span>

<span data-ttu-id="28fa3-105">**\_ \_ Второй макрос MCI тмсф** извлекает компонент секунд из параметра, содержащего Упакованные дорожки/минуты/секунды/кадры (тмсф).</span><span class="sxs-lookup"><span data-stu-id="28fa3-105">The **MCI\_TMSF\_SECOND** macro retrieves the seconds component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fa3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28fa3-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="28fa3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="28fa3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28fa3-108">*двтмсф*</span><span class="sxs-lookup"><span data-stu-id="28fa3-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="28fa3-109">Время в формате ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="28fa3-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28fa3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28fa3-110">Return value</span></span>

<span data-ttu-id="28fa3-111">Возвращает компонент секунд указанной информации ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="28fa3-111">Returns the seconds component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="28fa3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28fa3-112">Remarks</span></span>

<span data-ttu-id="28fa3-113">Время в формате ТМСФ выражается как значение **DWORD** с наименьшим значащим байтом, содержащим дорожки, следующий младший значащий байт, содержащий минуты, следующий младший значащий байт, содержащий секунды, и самый значащий байт, содержащий кадры.</span><span class="sxs-lookup"><span data-stu-id="28fa3-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="28fa3-114">**Второй макрос \_ тмсф \_ MCI** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28fa3-114">The **MCI\_TMSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="28fa3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="28fa3-115">Requirements</span></span>



| <span data-ttu-id="28fa3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="28fa3-116">Requirement</span></span> | <span data-ttu-id="28fa3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="28fa3-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28fa3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28fa3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="28fa3-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28fa3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28fa3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28fa3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="28fa3-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28fa3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="28fa3-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28fa3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="28fa3-123"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="28fa3-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28fa3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28fa3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fa3-125">MCI</span><span class="sxs-lookup"><span data-stu-id="28fa3-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="28fa3-126">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="28fa3-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





