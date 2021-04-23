---
title: Структура MCI_INFO_PARMS (МЦиапи. h)
description: '\_Структура пармс сведения о MCI \_ содержит сведения о команде MCI \_ info.'
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- MCI_INFO_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493035"
---
# <a name="mci_info_parms-structure"></a><span data-ttu-id="6b4c3-104">\_ \_ Структура ПАРМС сведений MCI</span><span class="sxs-lookup"><span data-stu-id="6b4c3-104">MCI\_INFO\_PARMS structure</span></span>

<span data-ttu-id="6b4c3-105">Структура **\_ \_ Пармс сведения о MCI** содержит сведения о команде [**MCI \_ info**](mci-info.md) .</span><span class="sxs-lookup"><span data-stu-id="6b4c3-105">The **MCI\_INFO\_PARMS** structure contains information for the [**MCI\_INFO**](mci-info.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b4c3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b4c3-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="6b4c3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6b4c3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b4c3-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6b4c3-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6b4c3-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="6b4c3-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6b4c3-110">**лпстрретурн**</span><span class="sxs-lookup"><span data-stu-id="6b4c3-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="6b4c3-111">Буфер для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="6b4c3-111">Buffer for return string.</span></span>

</dd> <dt>

<span data-ttu-id="6b4c3-112">**двретсизе**</span><span class="sxs-lookup"><span data-stu-id="6b4c3-112">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="6b4c3-113">Размер возвращаемой строки в символах.</span><span class="sxs-lookup"><span data-stu-id="6b4c3-113">Size, in characters, of return string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b4c3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b4c3-114">Remarks</span></span>

<span data-ttu-id="6b4c3-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="6b4c3-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b4c3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6b4c3-116">Requirements</span></span>



| <span data-ttu-id="6b4c3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6b4c3-117">Requirement</span></span> | <span data-ttu-id="6b4c3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6b4c3-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4c3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b4c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b4c3-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b4c3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6b4c3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b4c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b4c3-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b4c3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b4c3-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b4c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b4c3-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b4c3-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b4c3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b4c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b4c3-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6b4c3-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6b4c3-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="6b4c3-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6b4c3-128">**\_сведения о MCI**</span><span class="sxs-lookup"><span data-stu-id="6b4c3-128">**MCI\_INFO**</span></span>](mci-info.md)
</dt> <dt>

<span data-ttu-id="6b4c3-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b4c3-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

