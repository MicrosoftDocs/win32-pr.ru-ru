---
title: Структура MCI_GETDEVCAPS_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI жетдевкапс содержит сведения о устройства для команды MCI \_ жетдевкапс.'
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- MCI_GETDEVCAPS_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071317"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="cf409-104">\_ \_ Структура пармс MCI жетдевкапс</span><span class="sxs-lookup"><span data-stu-id="cf409-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="cf409-105">Структура **\_ \_ пармс MCI жетдевкапс** содержит сведения о устройства для команды [**MCI \_ жетдевкапс**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="cf409-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf409-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf409-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="cf409-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cf409-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf409-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cf409-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="cf409-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="cf409-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="cf409-110">**двретурн**</span><span class="sxs-lookup"><span data-stu-id="cf409-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="cf409-111">Содержит сведения о выходе.</span><span class="sxs-lookup"><span data-stu-id="cf409-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="cf409-112">**двитем**</span><span class="sxs-lookup"><span data-stu-id="cf409-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="cf409-113">Запрашиваемая возможность.</span><span class="sxs-lookup"><span data-stu-id="cf409-113">Capability being queried.</span></span> <span data-ttu-id="cf409-114">Этот элемент может быть одной из констант, перечисленных в справочном материале для команды [**MCI \_ жетдевкапс**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="cf409-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf409-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf409-115">Remarks</span></span>

<span data-ttu-id="cf409-116">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="cf409-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf409-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cf409-117">Requirements</span></span>



| <span data-ttu-id="cf409-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cf409-118">Requirement</span></span> | <span data-ttu-id="cf409-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cf409-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf409-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf409-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cf409-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf409-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cf409-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf409-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cf409-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf409-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf409-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf409-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf409-125"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf409-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf409-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf409-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf409-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="cf409-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cf409-128">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="cf409-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="cf409-129">**\_ЖЕТДЕВКАПС MCI**</span><span class="sxs-lookup"><span data-stu-id="cf409-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="cf409-130">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf409-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

