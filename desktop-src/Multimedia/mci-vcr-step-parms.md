---
title: Структура MCI_VCR_STEP_PARMS (видеомагнитофон. h)
description: '\_Структура шага пармс видеомагнитофона MCI \_ \_ содержит параметры для \_ команды шага MCI для устройств записи видеокассет.'
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071235"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="f6cc0-104">\_ \_ Пармсная структура шага видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="f6cc0-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="f6cc0-105">Структура **\_ \_ шага \_ Пармс видеомагнитофона MCI** содержит параметры для [**команды \_ шага MCI**](mci-step.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="f6cc0-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6cc0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6cc0-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="f6cc0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f6cc0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6cc0-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f6cc0-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="f6cc0-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="f6cc0-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="f6cc0-110">**двфрамес**</span><span class="sxs-lookup"><span data-stu-id="f6cc0-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="f6cc0-111">Число кадров для перехода (длина одного шага) по мере выполнения командой [**\_ шага MCI**](mci-step.md) шага вперед или назад по содержимому.</span><span class="sxs-lookup"><span data-stu-id="f6cc0-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6cc0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6cc0-112">Remarks</span></span>

<span data-ttu-id="f6cc0-113">При назначении данных элементам этой структуры установите соответствующие флаги в параметре *Фдвкомманд* [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="f6cc0-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6cc0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f6cc0-114">Requirements</span></span>



| <span data-ttu-id="f6cc0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f6cc0-115">Requirement</span></span> | <span data-ttu-id="f6cc0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6cc0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f6cc0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6cc0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6cc0-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6cc0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f6cc0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6cc0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6cc0-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6cc0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f6cc0-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f6cc0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6cc0-122"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6cc0-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6cc0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6cc0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6cc0-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="f6cc0-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f6cc0-125">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="f6cc0-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="f6cc0-126">**\_шаг MCI**</span><span class="sxs-lookup"><span data-stu-id="f6cc0-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="f6cc0-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6cc0-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

