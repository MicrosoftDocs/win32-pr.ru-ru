---
title: Структура MCI_VCR_STATUS_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс состояния видеомагнитофона MCI \_ содержит параметры команды "состояние MCI" \_ для устройств записи видеокассет.'
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988262"
---
# <a name="mci_vcr_status_parms-structure"></a><span data-ttu-id="05dd9-104">\_ \_ Структура пармс состояния видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="05dd9-104">MCI\_VCR\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="05dd9-105">Структура **\_ \_ \_ пармс состояния видеомагнитофона MCI** содержит параметры команды " [**\_ состояние MCI**](mci-status.md) " для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="05dd9-105">The **MCI\_VCR\_STATUS\_PARMS** structure contains parameters for the [**MCI\_STATUS**](mci-status.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="05dd9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05dd9-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="05dd9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="05dd9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="05dd9-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="05dd9-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="05dd9-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="05dd9-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="05dd9-110">**двретурн**</span><span class="sxs-lookup"><span data-stu-id="05dd9-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="05dd9-111">Значение, возвращаемое командой " [**\_ состояние MCI**](mci-status.md) ".</span><span class="sxs-lookup"><span data-stu-id="05dd9-111">Value returned by the [**MCI\_STATUS**](mci-status.md) command.</span></span> <span data-ttu-id="05dd9-112">Возвращаемое значение зависит от запроса команды.</span><span class="sxs-lookup"><span data-stu-id="05dd9-112">The return value varies according to the inquiry of the command.</span></span> <span data-ttu-id="05dd9-113">Дополнительные сведения см. в описании команды [**\_ состояния MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="05dd9-113">For more information, see the description of the [**MCI\_STATUS**](mci-status-parms.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="05dd9-114">**двитем**</span><span class="sxs-lookup"><span data-stu-id="05dd9-114">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="05dd9-115">Тип запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="05dd9-115">Type of information requested.</span></span>

</dd> <dt>

<span data-ttu-id="05dd9-116">**двтракк**</span><span class="sxs-lookup"><span data-stu-id="05dd9-116">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="05dd9-117">Звуковая или видеодорожка, которая будет хранить информацию во время следующей записи.</span><span class="sxs-lookup"><span data-stu-id="05dd9-117">Audio or video track that will store information during the next recording.</span></span> <span data-ttu-id="05dd9-118">Этот элемент используется для возврата сведений, когда команда [**MCI \_ Status**](mci-status-parms.md) выдает запрос о состоянии записи видео или звука.</span><span class="sxs-lookup"><span data-stu-id="05dd9-118">This member is used to return information when the [**MCI\_STATUS**](mci-status-parms.md) command inquires about the video or audio recording status.</span></span>

</dd> <dt>

<span data-ttu-id="05dd9-119">**двнумбер**</span><span class="sxs-lookup"><span data-stu-id="05dd9-119">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="05dd9-120">Логический тюнер, с которым связан текущий канал.</span><span class="sxs-lookup"><span data-stu-id="05dd9-120">Logical tuner that the current channel is associated with.</span></span> <span data-ttu-id="05dd9-121">Этот элемент используется для возврата сведений, когда команда [**MCI \_ Status**](mci-status.md) запрашивать сведения о текущем номере канала.</span><span class="sxs-lookup"><span data-stu-id="05dd9-121">This member is used to return information when the [**MCI\_STATUS**](mci-status.md) command inquires about the current channel number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05dd9-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05dd9-122">Remarks</span></span>

<span data-ttu-id="05dd9-123">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="05dd9-123">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="05dd9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="05dd9-124">Requirements</span></span>



| <span data-ttu-id="05dd9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="05dd9-125">Requirement</span></span> | <span data-ttu-id="05dd9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="05dd9-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="05dd9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05dd9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="05dd9-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05dd9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="05dd9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05dd9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="05dd9-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05dd9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05dd9-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="05dd9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="05dd9-132"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="05dd9-132"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05dd9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05dd9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05dd9-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="05dd9-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="05dd9-135">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="05dd9-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="05dd9-136">**\_состояние MCI**</span><span class="sxs-lookup"><span data-stu-id="05dd9-136">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="05dd9-137">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="05dd9-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

