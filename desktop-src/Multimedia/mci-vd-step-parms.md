---
title: Структура MCI_VD_STEP_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс VD шага MCI \_ содержит сведения о \_ команде шага MCI для устройств видеодиск.'
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- MCI_VD_STEP_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534199"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="02eda-104">\_ \_ Структура пармс VD для шага MCI \_</span><span class="sxs-lookup"><span data-stu-id="02eda-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="02eda-105">Структура **\_ пармс VD \_ шага \_ MCI** содержит сведения о команде [**\_ шага MCI**](mci-step.md) для устройств видеодиск.</span><span class="sxs-lookup"><span data-stu-id="02eda-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="02eda-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02eda-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="02eda-107">Члены</span><span class="sxs-lookup"><span data-stu-id="02eda-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="02eda-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="02eda-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="02eda-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="02eda-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="02eda-110">**двфрамес**</span><span class="sxs-lookup"><span data-stu-id="02eda-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="02eda-111">Число кадров для шага.</span><span class="sxs-lookup"><span data-stu-id="02eda-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02eda-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02eda-112">Remarks</span></span>

<span data-ttu-id="02eda-113">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="02eda-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="02eda-114">Требования</span><span class="sxs-lookup"><span data-stu-id="02eda-114">Requirements</span></span>



| <span data-ttu-id="02eda-115">Требование</span><span class="sxs-lookup"><span data-stu-id="02eda-115">Requirement</span></span> | <span data-ttu-id="02eda-116">Значение</span><span class="sxs-lookup"><span data-stu-id="02eda-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02eda-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02eda-117">Minimum supported client</span></span><br/> | <span data-ttu-id="02eda-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02eda-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="02eda-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02eda-119">Minimum supported server</span></span><br/> | <span data-ttu-id="02eda-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02eda-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="02eda-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="02eda-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="02eda-122"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="02eda-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02eda-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02eda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02eda-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="02eda-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="02eda-125">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="02eda-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="02eda-126">**\_шаг MCI**</span><span class="sxs-lookup"><span data-stu-id="02eda-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="02eda-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02eda-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

