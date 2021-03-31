---
title: Структура MCI_VCR_PLAY_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс ВИДЕОМАГНИТОФОНА воспроизведения MCI \_ содержит параметры для \_ команды MCI Play для устройств записи видеокассет.'
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988763"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="d1603-104">Видеомагнитофон MCI \_ \_ воспроизводит \_ структуру пармс</span><span class="sxs-lookup"><span data-stu-id="d1603-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="d1603-105">Структура **\_ пармс видеомагнитофона \_ воспроизведения \_ MCI** содержит параметры для команды [**MCI \_ Play**](mci-play.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="d1603-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1603-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1603-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="d1603-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d1603-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1603-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="d1603-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d1603-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="d1603-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d1603-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="d1603-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="d1603-111">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d1603-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="d1603-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="d1603-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="d1603-113">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d1603-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="d1603-114">**дват**</span><span class="sxs-lookup"><span data-stu-id="d1603-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="d1603-115">Значение времени, влияющее на команду [**MCI \_ Play**](mci-play.md) или командную [**\_ очередь MCI**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="d1603-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="d1603-116">Для [**\_ воспроизведения MCI**](mci-play-parms.md)это время начала воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d1603-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="d1603-117">В случае с MCI, это время, когда устройство куед достигает места, указанного в **двфром**. **\_**</span><span class="sxs-lookup"><span data-stu-id="d1603-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1603-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1603-118">Remarks</span></span>

<span data-ttu-id="d1603-119">Позиции указываются в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="d1603-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="d1603-120">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="d1603-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1603-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d1603-121">Requirements</span></span>



| <span data-ttu-id="d1603-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d1603-122">Requirement</span></span> | <span data-ttu-id="d1603-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d1603-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d1603-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1603-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1603-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d1603-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d1603-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1603-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1603-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d1603-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d1603-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d1603-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1603-129"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1603-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1603-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1603-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1603-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d1603-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d1603-132">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="d1603-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d1603-133">**\_Подсказка MCI**</span><span class="sxs-lookup"><span data-stu-id="d1603-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="d1603-134">**\_Воспроизведение MCI**</span><span class="sxs-lookup"><span data-stu-id="d1603-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="d1603-135">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1603-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

