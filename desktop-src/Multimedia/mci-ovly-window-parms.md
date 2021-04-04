---
title: Структура MCI_OVLY_WINDOW_PARMS (МЦиапи. h)
description: '\_ \_ Структура ПАРМС окна MCI овли \_ содержит отображаемую информацию для \_ команды окна MCI для устройств наложения видео.'
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988177"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="bb7cf-104">\_ \_ Структура ПАРМС окна MCI овли \_</span><span class="sxs-lookup"><span data-stu-id="bb7cf-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="bb7cf-105">Структура **\_ \_ \_ пармс окна MCI овли** содержит отображаемую информацию для команды [**\_ окна MCI**](mci-window.md) для устройств наложения видео.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7cf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb7cf-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="bb7cf-107">Члены</span><span class="sxs-lookup"><span data-stu-id="bb7cf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb7cf-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bb7cf-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bb7cf-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="bb7cf-111">Маркер для отображаемого окна.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="bb7cf-112">**нкмдшов**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="bb7cf-113">Команда для вывода окна.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="bb7cf-114">**лпстртекст**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="bb7cf-115">Заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb7cf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb7cf-116">Remarks</span></span>

<span data-ttu-id="bb7cf-117">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7cf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bb7cf-118">Requirements</span></span>



| <span data-ttu-id="bb7cf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bb7cf-119">Requirement</span></span> | <span data-ttu-id="bb7cf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bb7cf-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7cf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb7cf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7cf-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb7cf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb7cf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb7cf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7cf-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb7cf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bb7cf-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bb7cf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb7cf-126"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb7cf-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7cf-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb7cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7cf-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bb7cf-129">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bb7cf-130">**\_окно MCI**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="bb7cf-131">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb7cf-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

