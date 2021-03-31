---
title: Структура MCI_OVLY_LOAD_PARMS (Ммсистем. h)
description: '\_ \_ Структура ПАРМС загрузки MCI овли \_ содержит сведения для \_ команды MCI Load для устройств наложения видео.'
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071094"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="28d49-104">\_ \_ Структура ПАРМС загрузки MCI овли \_</span><span class="sxs-lookup"><span data-stu-id="28d49-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="28d49-105">Структура **\_ \_ \_ пармс загрузки MCI овли** содержит сведения для команды [**MCI \_ Load**](mci-load.md) для устройств наложения видео.</span><span class="sxs-lookup"><span data-stu-id="28d49-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d49-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28d49-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="28d49-107">Члены</span><span class="sxs-lookup"><span data-stu-id="28d49-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="28d49-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="28d49-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="28d49-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="28d49-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="28d49-110">**лпфиленаме**</span><span class="sxs-lookup"><span data-stu-id="28d49-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="28d49-111">Имя загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="28d49-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="28d49-112">**RC**</span><span class="sxs-lookup"><span data-stu-id="28d49-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="28d49-113">Определяет область обновляемого буфера видео.</span><span class="sxs-lookup"><span data-stu-id="28d49-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="28d49-114">Структуры [Rect](/previous-versions//ms536136(v=vs.85)) в MCI обрабатываются по-разному, чем в других частях Windows. в MCI, **RC. Right** содержит ширину прямоугольника и **RC. Bottom** содержит его высоту.</span><span class="sxs-lookup"><span data-stu-id="28d49-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28d49-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28d49-115">Remarks</span></span>

<span data-ttu-id="28d49-116">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="28d49-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d49-117">Требования</span><span class="sxs-lookup"><span data-stu-id="28d49-117">Requirements</span></span>



| <span data-ttu-id="28d49-118">Требование</span><span class="sxs-lookup"><span data-stu-id="28d49-118">Requirement</span></span> | <span data-ttu-id="28d49-119">Значение</span><span class="sxs-lookup"><span data-stu-id="28d49-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28d49-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28d49-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28d49-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28d49-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="28d49-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28d49-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28d49-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28d49-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28d49-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28d49-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d49-125"><dt>Ммсистем. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d49-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d49-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28d49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d49-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="28d49-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="28d49-128">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="28d49-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="28d49-129">**\_Загрузка MCI**</span><span class="sxs-lookup"><span data-stu-id="28d49-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="28d49-130">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28d49-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="28d49-131">[ПЕРЕТАСКИВАЕМЫЕ](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28d49-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

