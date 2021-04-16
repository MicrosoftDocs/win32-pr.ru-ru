---
title: Макрос MCI_MSF_MINUTE (МЦиапи. h)
description: Макрос MCI \_ MSF \_ Minute извлекает компонент минут из параметра, содержащего Упакованные минуты/секунды/кадры (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650396"
---
# <a name="mci_msf_minute-macro"></a><span data-ttu-id="600f4-104">Макрос для платформы MCI ( \_ \_ минуту)</span><span class="sxs-lookup"><span data-stu-id="600f4-104">MCI\_MSF\_MINUTE macro</span></span>

<span data-ttu-id="600f4-105">Макрос **MCI \_ MSF \_ Minute** извлекает компонент минут из параметра, содержащего Упакованные минуты/секунды/кадры (MSF).</span><span class="sxs-lookup"><span data-stu-id="600f4-105">The **MCI\_MSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="600f4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="600f4-106">Syntax</span></span>


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="600f4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="600f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="600f4-108">*двмсф*</span><span class="sxs-lookup"><span data-stu-id="600f4-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="600f4-109">Время в формате MSF.</span><span class="sxs-lookup"><span data-stu-id="600f4-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="600f4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="600f4-110">Return value</span></span>

<span data-ttu-id="600f4-111">Возвращает компонент минут указанной информации MSF.</span><span class="sxs-lookup"><span data-stu-id="600f4-111">Returns the minutes component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="600f4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="600f4-112">Remarks</span></span>

<span data-ttu-id="600f4-113">Время в формате MSF выражается в виде значения **типа DWORD** с наименьшим значащим байтом, содержащим минуты, следующим наименее значащим байтом, содержащим секунды, и следующим наименьшим значащим байтом, содержащим кадры.</span><span class="sxs-lookup"><span data-stu-id="600f4-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="600f4-114">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="600f4-114">The most significant byte is unused.</span></span>

<span data-ttu-id="600f4-115">Макрос **MCI \_ MSF \_ Minute** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="600f4-115">The **MCI\_MSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a><span data-ttu-id="600f4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="600f4-116">Requirements</span></span>



| <span data-ttu-id="600f4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="600f4-117">Requirement</span></span> | <span data-ttu-id="600f4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="600f4-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="600f4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="600f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="600f4-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="600f4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="600f4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="600f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="600f4-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="600f4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="600f4-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="600f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="600f4-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="600f4-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600f4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="600f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600f4-126">MCI</span><span class="sxs-lookup"><span data-stu-id="600f4-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="600f4-127">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="600f4-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





