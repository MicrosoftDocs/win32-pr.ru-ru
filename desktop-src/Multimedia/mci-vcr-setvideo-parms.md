---
title: Структура MCI_VCR_SETVIDEO_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс СЕТВИДЕО видеомагнитофона MCI \_ содержит параметры для \_ команды MCI сетвидео для устройств записи видеокассет.'
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892513"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="26140-104">\_Структура пармс видеомагнитофона MCI \_ сетвидео \_</span><span class="sxs-lookup"><span data-stu-id="26140-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="26140-105">Структура **\_ \_ \_ пармс сетвидео видеомагнитофона MCI** содержит параметры для команды [**MCI \_ сетвидео**](mci-setvideo.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="26140-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="26140-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26140-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="26140-107">Члены</span><span class="sxs-lookup"><span data-stu-id="26140-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="26140-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="26140-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="26140-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="26140-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="26140-110">**двтракк**</span><span class="sxs-lookup"><span data-stu-id="26140-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="26140-111">Затронутая запись.</span><span class="sxs-lookup"><span data-stu-id="26140-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="26140-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="26140-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="26140-113">Тип входных данных или наблюдаемых входных данных.</span><span class="sxs-lookup"><span data-stu-id="26140-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="26140-114">**двнумбер**</span><span class="sxs-lookup"><span data-stu-id="26140-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="26140-115">Входные данные видео (для типа, указанного в элементе **двто** ) для использования.</span><span class="sxs-lookup"><span data-stu-id="26140-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26140-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26140-116">Remarks</span></span>

<span data-ttu-id="26140-117">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="26140-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="26140-118">Требования</span><span class="sxs-lookup"><span data-stu-id="26140-118">Requirements</span></span>



| <span data-ttu-id="26140-119">Требование</span><span class="sxs-lookup"><span data-stu-id="26140-119">Requirement</span></span> | <span data-ttu-id="26140-120">Значение</span><span class="sxs-lookup"><span data-stu-id="26140-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="26140-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26140-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26140-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26140-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="26140-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26140-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26140-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26140-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="26140-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="26140-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26140-126"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="26140-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26140-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26140-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26140-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="26140-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="26140-129">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="26140-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="26140-130">**\_СЕТВИДЕО MCI**</span><span class="sxs-lookup"><span data-stu-id="26140-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="26140-131">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26140-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

