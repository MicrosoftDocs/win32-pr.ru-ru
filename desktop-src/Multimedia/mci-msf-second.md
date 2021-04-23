---
title: Макрос MCI_MSF_SECOND (МЦиапи. h)
description: '\_ \_ Второй макрос MCI MSF получает компонент секунд из параметра, содержащего Упакованные минуты/секунды/кадры (MSF).'
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND макросов Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892105"
---
# <a name="mci_msf_second-macro"></a><span data-ttu-id="3df13-104">\_ \_ Второй макрос MCI MSF</span><span class="sxs-lookup"><span data-stu-id="3df13-104">MCI\_MSF\_SECOND macro</span></span>

<span data-ttu-id="3df13-105">**\_ \_ Второй макрос MCI MSF** получает компонент секунд из параметра, содержащего Упакованные минуты/секунды/кадры (MSF).</span><span class="sxs-lookup"><span data-stu-id="3df13-105">The **MCI\_MSF\_SECOND** macro retrieves the seconds component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df13-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3df13-106">Syntax</span></span>


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="3df13-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3df13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df13-108">*двмсф*</span><span class="sxs-lookup"><span data-stu-id="3df13-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="3df13-109">Время в формате MSF.</span><span class="sxs-lookup"><span data-stu-id="3df13-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df13-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3df13-110">Return value</span></span>

<span data-ttu-id="3df13-111">Возвращает компонент секунд указанной информации MSF.</span><span class="sxs-lookup"><span data-stu-id="3df13-111">Returns the seconds component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="3df13-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3df13-112">Remarks</span></span>

<span data-ttu-id="3df13-113">Время в формате MSF выражается в виде значения **типа DWORD** с наименьшим значащим байтом, содержащим минуты, следующим наименее значащим байтом, содержащим секунды, и следующим наименьшим значащим байтом, содержащим кадры.</span><span class="sxs-lookup"><span data-stu-id="3df13-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="3df13-114">Наиболее значимый байт не используется.</span><span class="sxs-lookup"><span data-stu-id="3df13-114">The most significant byte is unused.</span></span>

<span data-ttu-id="3df13-115">**\_ \_ Второй макрос MCI MSF** может быть определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3df13-115">The **MCI\_MSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="3df13-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3df13-116">Requirements</span></span>



| <span data-ttu-id="3df13-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3df13-117">Requirement</span></span> | <span data-ttu-id="3df13-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3df13-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3df13-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3df13-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3df13-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3df13-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3df13-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3df13-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3df13-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3df13-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3df13-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3df13-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df13-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df13-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df13-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3df13-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df13-126">MCI</span><span class="sxs-lookup"><span data-stu-id="3df13-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3df13-127">Макросы MCI</span><span class="sxs-lookup"><span data-stu-id="3df13-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





