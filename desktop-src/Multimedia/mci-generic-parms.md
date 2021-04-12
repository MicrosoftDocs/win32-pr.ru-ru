---
title: Структура MCI_GENERIC_PARMS (МЦиапи. h)
description: '\_Общая \_ Структура пармс MCI содержит маркер окна, принимающего сообщения уведомления. Эта структура используется для командных сообщений MCI с пустыми списками параметров.'
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490122"
---
# <a name="mci_generic_parms-structure"></a><span data-ttu-id="51272-105">\_Универсальная \_ Структура пармс MCI</span><span class="sxs-lookup"><span data-stu-id="51272-105">MCI\_GENERIC\_PARMS structure</span></span>

<span data-ttu-id="51272-106">**Общая структура \_ \_ пармс MCI** содержит маркер окна, принимающего сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="51272-106">The **MCI\_GENERIC\_PARMS** structure contains the handle of the window that receives notification messages.</span></span> <span data-ttu-id="51272-107">Эта структура используется для командных сообщений MCI с пустыми списками параметров.</span><span class="sxs-lookup"><span data-stu-id="51272-107">This structure is used for MCI command messages that have empty parameter lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="51272-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51272-108">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a><span data-ttu-id="51272-109">Члены</span><span class="sxs-lookup"><span data-stu-id="51272-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="51272-110">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="51272-110">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="51272-111">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="51272-111">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51272-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51272-112">Remarks</span></span>

<span data-ttu-id="51272-113">Пармс и MCI **\_ закрывают \_** структуры **\_ \_ пармс** , идентичные структурам **\_ универсального \_ пармс MCI** .</span><span class="sxs-lookup"><span data-stu-id="51272-113">The **MCI\_CLOSE\_PARMS** and **MCI\_REALIZE\_PARMS** structures are identical to the **MCI\_GENERIC\_PARMS** structure.</span></span>

<span data-ttu-id="51272-114">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="51272-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="51272-115">Требования</span><span class="sxs-lookup"><span data-stu-id="51272-115">Requirements</span></span>



| <span data-ttu-id="51272-116">Требование</span><span class="sxs-lookup"><span data-stu-id="51272-116">Requirement</span></span> | <span data-ttu-id="51272-117">Значение</span><span class="sxs-lookup"><span data-stu-id="51272-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="51272-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51272-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51272-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51272-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="51272-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51272-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51272-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51272-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51272-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51272-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51272-123"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="51272-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51272-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51272-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51272-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="51272-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="51272-126">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="51272-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

<span data-ttu-id="51272-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51272-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

