---
title: Структура MCI_SET_PARMS (МЦиапи. h)
description: '\_ \_ Структура ПАРМС набора MCI содержит сведения для \_ команды MCI Set.'
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- MCI_SET_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071312"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="988f5-104">\_ \_ Структура ПАРМС набора MCI</span><span class="sxs-lookup"><span data-stu-id="988f5-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="988f5-105">Структура **\_ \_ пармс набора MCI** содержит сведения для команды [**MCI \_ Set**](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="988f5-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="988f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="988f5-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="988f5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="988f5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="988f5-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="988f5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="988f5-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="988f5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="988f5-110">**двтимеформат**</span><span class="sxs-lookup"><span data-stu-id="988f5-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="988f5-111">Формат времени для устройства.</span><span class="sxs-lookup"><span data-stu-id="988f5-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="988f5-112">**дваудио**</span><span class="sxs-lookup"><span data-stu-id="988f5-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="988f5-113">Канал вывода звука.</span><span class="sxs-lookup"><span data-stu-id="988f5-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="988f5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="988f5-114">Remarks</span></span>

<span data-ttu-id="988f5-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="988f5-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="988f5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="988f5-116">Requirements</span></span>



| <span data-ttu-id="988f5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="988f5-117">Requirement</span></span> | <span data-ttu-id="988f5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="988f5-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="988f5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="988f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="988f5-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="988f5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="988f5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="988f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="988f5-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="988f5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="988f5-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="988f5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="988f5-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="988f5-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="988f5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="988f5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="988f5-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="988f5-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="988f5-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="988f5-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="988f5-128">**\_набор MCI**</span><span class="sxs-lookup"><span data-stu-id="988f5-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="988f5-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="988f5-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

