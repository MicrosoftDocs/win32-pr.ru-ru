---
title: Структура MCI_OVLY_RECT_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс MCI овли Rect \_ содержит сведения о размещении для MCI \_ и MCI, \_ где команды для устройств с наложением видео.'
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488985"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="10db1-104">\_Структура пармс для MCI овли \_ Rect \_</span><span class="sxs-lookup"><span data-stu-id="10db1-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="10db1-105">Структура **\_ \_ \_ пармс MCI овли Rect** содержит сведения о размещении для [**MCI \_**](mci-put.md) и [**MCI, \_ где**](mci-where.md) команды для устройств с наложением видео.</span><span class="sxs-lookup"><span data-stu-id="10db1-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="10db1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10db1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="10db1-107">Члены</span><span class="sxs-lookup"><span data-stu-id="10db1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="10db1-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="10db1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="10db1-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="10db1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="10db1-110">**RC**</span><span class="sxs-lookup"><span data-stu-id="10db1-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="10db1-111">Прямоугольник, содержащий сведения о размещении.</span><span class="sxs-lookup"><span data-stu-id="10db1-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="10db1-112">Структуры [Rect](/previous-versions//ms536136(v=vs.85)) в MCI обрабатываются по-разному, чем в других частях Windows. в MCI, **RC. Right** содержит ширину прямоугольника и **RC. Bottom** содержит его высоту.</span><span class="sxs-lookup"><span data-stu-id="10db1-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10db1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10db1-113">Remarks</span></span>

<span data-ttu-id="10db1-114">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="10db1-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="10db1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="10db1-115">Requirements</span></span>



| <span data-ttu-id="10db1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="10db1-116">Requirement</span></span> | <span data-ttu-id="10db1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="10db1-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10db1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10db1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10db1-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10db1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="10db1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10db1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10db1-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10db1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="10db1-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="10db1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10db1-123"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="10db1-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10db1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10db1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10db1-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="10db1-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="10db1-126">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="10db1-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="10db1-127">**\_Добавление MCI**</span><span class="sxs-lookup"><span data-stu-id="10db1-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="10db1-128">**MCI, \_ где**</span><span class="sxs-lookup"><span data-stu-id="10db1-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="10db1-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10db1-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="10db1-130">[ПЕРЕТАСКИВАЕМЫЕ](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10db1-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

