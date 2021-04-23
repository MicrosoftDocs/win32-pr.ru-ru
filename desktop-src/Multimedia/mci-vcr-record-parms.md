---
title: Структура MCI_VCR_RECORD_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс записи видеомагнитофона MCI \_ содержит параметры для \_ команды записи MCI для устройств записи видеокассет.'
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672608"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="dee3b-104">\_ \_ Структура пармс записи видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="dee3b-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="dee3b-105">Структура **\_ \_ \_ пармс записи видеомагнитофона MCI** содержит параметры для команды [**\_ записи MCI**](mci-record.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="dee3b-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee3b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dee3b-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="dee3b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="dee3b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dee3b-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="dee3b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="dee3b-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="dee3b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="dee3b-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="dee3b-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="dee3b-111">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dee3b-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="dee3b-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="dee3b-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="dee3b-113">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dee3b-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="dee3b-114">**дват**</span><span class="sxs-lookup"><span data-stu-id="dee3b-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="dee3b-115">Значение времени, которое влияет [**на \_ запись MCI**](mci-record.md) или команду [**MCI \_ Cue**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="dee3b-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="dee3b-116">Для **\_ записи MCI** это время начала записи.</span><span class="sxs-lookup"><span data-stu-id="dee3b-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="dee3b-117">В случае с MCI, это время, когда устройство куед достигает места, указанного в **двфром**. **\_**</span><span class="sxs-lookup"><span data-stu-id="dee3b-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dee3b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dee3b-118">Remarks</span></span>

<span data-ttu-id="dee3b-119">Позиции указываются в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="dee3b-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="dee3b-120">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="dee3b-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee3b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dee3b-121">Requirements</span></span>



| <span data-ttu-id="dee3b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dee3b-122">Requirement</span></span> | <span data-ttu-id="dee3b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dee3b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dee3b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dee3b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dee3b-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dee3b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dee3b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dee3b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dee3b-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dee3b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dee3b-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dee3b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee3b-129"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee3b-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee3b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dee3b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee3b-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="dee3b-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dee3b-132">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="dee3b-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="dee3b-133">**\_Подсказка MCI**</span><span class="sxs-lookup"><span data-stu-id="dee3b-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="dee3b-134">**\_запись MCI**</span><span class="sxs-lookup"><span data-stu-id="dee3b-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="dee3b-135">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dee3b-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

