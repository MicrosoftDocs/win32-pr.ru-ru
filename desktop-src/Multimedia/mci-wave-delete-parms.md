---
title: Структура MCI_WAVE_DELETE_PARMS (МЦиапи. h)
description: Структура пармс "Wave" в MCI \_ \_ \_ содержит сведения о положении для \_ команды MCI DELETE для устройств аудио-аудио.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- MCI_WAVE_DELETE_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489576"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="33225-104">\_ \_ Структура пармс удаления волны MCI \_</span><span class="sxs-lookup"><span data-stu-id="33225-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="33225-105">Структура **\_ \_ \_ пармс "Wave** " в MCI содержит сведения о положении для команды [**MCI \_ Delete**](mci-delete.md) для устройств аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="33225-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="33225-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33225-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="33225-107">Члены</span><span class="sxs-lookup"><span data-stu-id="33225-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="33225-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="33225-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="33225-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="33225-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="33225-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="33225-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="33225-111">Расположение для удаления.</span><span class="sxs-lookup"><span data-stu-id="33225-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="33225-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="33225-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="33225-113">Расположение для удаления.</span><span class="sxs-lookup"><span data-stu-id="33225-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33225-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33225-114">Remarks</span></span>

<span data-ttu-id="33225-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="33225-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="33225-116">Требования</span><span class="sxs-lookup"><span data-stu-id="33225-116">Requirements</span></span>



| <span data-ttu-id="33225-117">Требование</span><span class="sxs-lookup"><span data-stu-id="33225-117">Requirement</span></span> | <span data-ttu-id="33225-118">Значение</span><span class="sxs-lookup"><span data-stu-id="33225-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33225-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33225-119">Minimum supported client</span></span><br/> | <span data-ttu-id="33225-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33225-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="33225-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33225-121">Minimum supported server</span></span><br/> | <span data-ttu-id="33225-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33225-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="33225-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="33225-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33225-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="33225-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33225-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33225-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33225-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="33225-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="33225-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="33225-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="33225-128">**\_Удаление MCI**</span><span class="sxs-lookup"><span data-stu-id="33225-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="33225-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33225-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

