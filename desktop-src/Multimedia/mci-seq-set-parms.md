---
title: Структура MCI_SEQ_SET_PARMS (МЦиапи. h)
description: Структура MCI \_ Seq \_ Set \_ пармс содержит сведения о \_ команде MCI Set для устройств MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988311"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="cac76-104">\_Структура MCI Seq \_ Set \_ пармс</span><span class="sxs-lookup"><span data-stu-id="cac76-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="cac76-105">Структура **MCI \_ Seq \_ Set \_ пармс** содержит сведения о команде [**MCI \_ Set**](mci-set.md) для устройств MIDI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="cac76-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac76-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cac76-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="cac76-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cac76-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cac76-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="cac76-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="cac76-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-110">**двтимеформат**</span><span class="sxs-lookup"><span data-stu-id="cac76-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-111">Формат времени программы Sequencer.</span><span class="sxs-lookup"><span data-stu-id="cac76-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-112">**дваудио**</span><span class="sxs-lookup"><span data-stu-id="cac76-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-113">Канал вывода звука.</span><span class="sxs-lookup"><span data-stu-id="cac76-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-114">**двтемпо**</span><span class="sxs-lookup"><span data-stu-id="cac76-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-115">Темп.</span><span class="sxs-lookup"><span data-stu-id="cac76-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-116">**двпорт**</span><span class="sxs-lookup"><span data-stu-id="cac76-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-117">порт;</span><span class="sxs-lookup"><span data-stu-id="cac76-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-118">**двславе**</span><span class="sxs-lookup"><span data-stu-id="cac76-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-119">Тип синхронизации, используемый секвенсором для подчиненной операции.</span><span class="sxs-lookup"><span data-stu-id="cac76-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-120">**двмастер**</span><span class="sxs-lookup"><span data-stu-id="cac76-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-121">Тип синхронизации, используемый программой Sequencer для главной операции.</span><span class="sxs-lookup"><span data-stu-id="cac76-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="cac76-122">**двоффсет**</span><span class="sxs-lookup"><span data-stu-id="cac76-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="cac76-123">Смещение данных.</span><span class="sxs-lookup"><span data-stu-id="cac76-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cac76-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cac76-124">Remarks</span></span>

<span data-ttu-id="cac76-125">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="cac76-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac76-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cac76-126">Requirements</span></span>



| <span data-ttu-id="cac76-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cac76-127">Requirement</span></span> | <span data-ttu-id="cac76-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cac76-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cac76-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cac76-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cac76-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cac76-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cac76-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cac76-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cac76-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cac76-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cac76-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cac76-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac76-134"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac76-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac76-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cac76-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac76-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="cac76-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cac76-137">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="cac76-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="cac76-138">**\_набор MCI**</span><span class="sxs-lookup"><span data-stu-id="cac76-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="cac76-139">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cac76-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

