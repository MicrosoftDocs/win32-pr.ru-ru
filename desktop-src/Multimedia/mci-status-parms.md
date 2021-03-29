---
title: Структура MCI_STATUS_PARMS (МЦиапи. h)
description: '\_ \_ Структура ПАРМС состояния MCI содержит сведения о \_ команде состояния MCI.'
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988310"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="4e1a0-104">\_ \_ Структура ПАРМС состояния MCI</span><span class="sxs-lookup"><span data-stu-id="4e1a0-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="4e1a0-105">Структура **\_ \_ пармс состояния MCI** содержит сведения о команде [**\_ состояния MCI**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="4e1a0-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e1a0-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="4e1a0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4e1a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e1a0-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4e1a0-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="4e1a0-110">**двретурн**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="4e1a0-111">Содержит сведения о возврате.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="4e1a0-112">**двитем**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="4e1a0-113">Запрашиваемая возможность.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="4e1a0-114">**двтракк**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="4e1a0-115">Длина или число дорожек.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e1a0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e1a0-116">Remarks</span></span>

<span data-ttu-id="4e1a0-117">\_ \_ Флаг элемента состояния MCI должен быть задан в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) для проверки элемента **двитем** , который должен содержать одну из констант, указывающих, какие сведения о состоянии запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="4e1a0-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1a0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4e1a0-118">Requirements</span></span>



| <span data-ttu-id="4e1a0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4e1a0-119">Requirement</span></span> | <span data-ttu-id="4e1a0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4e1a0-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1a0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e1a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1a0-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e1a0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4e1a0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e1a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1a0-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e1a0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4e1a0-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4e1a0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e1a0-126"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1a0-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1a0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e1a0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1a0-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4e1a0-129">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="4e1a0-130">**\_состояние MCI**</span><span class="sxs-lookup"><span data-stu-id="4e1a0-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="4e1a0-131">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e1a0-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

