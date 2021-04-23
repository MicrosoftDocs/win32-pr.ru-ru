---
title: Структура MCI_RECORD_PARMS (МЦиапи. h)
description: '\_ \_ Структура ПАРМС записи MCI содержит сведения о размещении для \_ команды MCI Record.'
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488979"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="fc2b8-104">\_ \_ Структура ПАРМС записи MCI</span><span class="sxs-lookup"><span data-stu-id="fc2b8-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="fc2b8-105">Структура **\_ \_ пармс записи MCI** содержит сведения о размещении для команды [**MCI \_ Record**](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="fc2b8-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2b8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc2b8-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="fc2b8-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fc2b8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc2b8-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="fc2b8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="fc2b8-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="fc2b8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="fc2b8-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="fc2b8-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="fc2b8-111">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc2b8-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="fc2b8-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="fc2b8-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="fc2b8-113">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fc2b8-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc2b8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc2b8-114">Remarks</span></span>

<span data-ttu-id="fc2b8-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="fc2b8-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2b8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fc2b8-116">Requirements</span></span>



| <span data-ttu-id="fc2b8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fc2b8-117">Requirement</span></span> | <span data-ttu-id="fc2b8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fc2b8-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2b8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc2b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2b8-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc2b8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fc2b8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc2b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2b8-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc2b8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fc2b8-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc2b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc2b8-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2b8-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2b8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc2b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2b8-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="fc2b8-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fc2b8-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="fc2b8-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="fc2b8-128">**\_запись MCI**</span><span class="sxs-lookup"><span data-stu-id="fc2b8-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="fc2b8-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc2b8-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

