---
title: Структура MCI_VCR_SETAUDIO_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс СЕТАУДИО видеомагнитофона MCI \_ содержит параметры для \_ команды MCI сетаудио для устройств записи видеокассет.'
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891553"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="42e62-104">\_Структура пармс видеомагнитофона MCI \_ сетаудио \_</span><span class="sxs-lookup"><span data-stu-id="42e62-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="42e62-105">Структура **\_ \_ \_ пармс сетаудио видеомагнитофона MCI** содержит параметры для команды [**MCI \_ сетаудио**](mci-setaudio.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="42e62-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e62-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42e62-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="42e62-107">Члены</span><span class="sxs-lookup"><span data-stu-id="42e62-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="42e62-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="42e62-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="42e62-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="42e62-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="42e62-110">**двтракк**</span><span class="sxs-lookup"><span data-stu-id="42e62-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="42e62-111">Звуковая дорожка.</span><span class="sxs-lookup"><span data-stu-id="42e62-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="42e62-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="42e62-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="42e62-113">Тип входных данных или наблюдаемых входных данных.</span><span class="sxs-lookup"><span data-stu-id="42e62-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="42e62-114">**двнумбер**</span><span class="sxs-lookup"><span data-stu-id="42e62-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="42e62-115">Использование звукового ввода (типа, указанного в элементе **двто** ) для использования.</span><span class="sxs-lookup"><span data-stu-id="42e62-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42e62-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42e62-116">Remarks</span></span>

<span data-ttu-id="42e62-117">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="42e62-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e62-118">Требования</span><span class="sxs-lookup"><span data-stu-id="42e62-118">Requirements</span></span>



| <span data-ttu-id="42e62-119">Требование</span><span class="sxs-lookup"><span data-stu-id="42e62-119">Requirement</span></span> | <span data-ttu-id="42e62-120">Значение</span><span class="sxs-lookup"><span data-stu-id="42e62-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42e62-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42e62-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42e62-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42e62-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42e62-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42e62-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42e62-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42e62-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42e62-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42e62-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e62-126"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e62-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e62-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42e62-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e62-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="42e62-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="42e62-129">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="42e62-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="42e62-130">**\_СЕТАУДИО MCI**</span><span class="sxs-lookup"><span data-stu-id="42e62-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="42e62-131">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42e62-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

