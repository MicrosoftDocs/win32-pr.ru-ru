---
title: Структура MCI_VCR_CUE_PARMS (видеомагнитофон. h)
description: '\_Структура Cue пармс на магнитофоне MCI \_ \_ содержит параметры для \_ команды MCI CUE для устройств записи видеокассет.'
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- MCI_VCR_CUE_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892581"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="475a2-104">\_ \_ Структура Cue пармс для видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="475a2-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="475a2-105">Структура **\_ \_ Cue \_ Пармс на магнитофоне MCI** содержит параметры для команды [**MCI \_ Cue**](mci-cue.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="475a2-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="475a2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="475a2-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="475a2-107">Члены</span><span class="sxs-lookup"><span data-stu-id="475a2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="475a2-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="475a2-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="475a2-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="475a2-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="475a2-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="475a2-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="475a2-111">Разместить в подсказке.</span><span class="sxs-lookup"><span data-stu-id="475a2-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="475a2-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="475a2-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="475a2-113">Разместить в подсказке.</span><span class="sxs-lookup"><span data-stu-id="475a2-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="475a2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="475a2-114">Remarks</span></span>

<span data-ttu-id="475a2-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="475a2-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="475a2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="475a2-116">Requirements</span></span>



| <span data-ttu-id="475a2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="475a2-117">Requirement</span></span> | <span data-ttu-id="475a2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="475a2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="475a2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="475a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="475a2-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="475a2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="475a2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="475a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="475a2-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="475a2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="475a2-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="475a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="475a2-124"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="475a2-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="475a2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="475a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475a2-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="475a2-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="475a2-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="475a2-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="475a2-128">**\_Подсказка MCI**</span><span class="sxs-lookup"><span data-stu-id="475a2-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="475a2-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="475a2-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

