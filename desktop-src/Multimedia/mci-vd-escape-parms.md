---
title: Структура MCI_VD_ESCAPE_PARMS (МЦиапи. h)
description: '\_ \_ Структура escape-пармс MCI VD \_ содержит команду, отправленную на устройство для \_ управляющей команды MCI для устройств видеодиск.'
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- MCI_VD_ESCAPE_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672623"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="3749d-104">\_ \_ Структура пармс escape-VD MCI \_</span><span class="sxs-lookup"><span data-stu-id="3749d-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="3749d-105">Структура **\_ Escape- \_ \_ пармс MCI VD** содержит команду, отправленную на устройство для [**\_ управляющей команды MCI**](mci-escape.md) для устройств видеодиск.</span><span class="sxs-lookup"><span data-stu-id="3749d-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3749d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3749d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="3749d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3749d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3749d-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3749d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3749d-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="3749d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3749d-110">**лпстркомманд**</span><span class="sxs-lookup"><span data-stu-id="3749d-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="3749d-111">Команда для отправки на устройство.</span><span class="sxs-lookup"><span data-stu-id="3749d-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3749d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3749d-112">Remarks</span></span>

<span data-ttu-id="3749d-113">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="3749d-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3749d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3749d-114">Requirements</span></span>



| <span data-ttu-id="3749d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3749d-115">Requirement</span></span> | <span data-ttu-id="3749d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3749d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3749d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3749d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3749d-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3749d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3749d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3749d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3749d-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3749d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3749d-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3749d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3749d-122"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3749d-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3749d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3749d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3749d-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3749d-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3749d-125">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="3749d-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3749d-126">**\_escape-последовательность MCI**</span><span class="sxs-lookup"><span data-stu-id="3749d-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="3749d-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3749d-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

