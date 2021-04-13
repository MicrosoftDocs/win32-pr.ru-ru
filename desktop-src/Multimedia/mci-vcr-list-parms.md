---
title: Структура MCI_VCR_LIST_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура пармс в списке видеомагнитофона видеомагнитофон \_ содержит параметры для команды MCI \_ List для устройств записи видеокассет.'
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- MCI_VCR_LIST_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341155"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="3c842-104">\_ \_ Структура пармс для списка видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="3c842-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="3c842-105">Структура **\_ пармс в \_ списке \_ видеомагнитофона видеомагнитофон** содержит параметры для команды [**MCI \_ List**](mci-list.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="3c842-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c842-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c842-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="3c842-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3c842-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c842-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3c842-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3c842-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="3c842-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3c842-110">**двретурн**</span><span class="sxs-lookup"><span data-stu-id="3c842-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="3c842-111">Буфер для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="3c842-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="3c842-112">**двнумбер**</span><span class="sxs-lookup"><span data-stu-id="3c842-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="3c842-113">Число видео или звуковых входов ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="3c842-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c842-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c842-114">Remarks</span></span>

<span data-ttu-id="3c842-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="3c842-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c842-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3c842-116">Requirements</span></span>



| <span data-ttu-id="3c842-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3c842-117">Requirement</span></span> | <span data-ttu-id="3c842-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3c842-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c842-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c842-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c842-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c842-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c842-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c842-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c842-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c842-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c842-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3c842-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c842-124"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c842-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c842-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c842-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c842-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3c842-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3c842-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="3c842-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3c842-128">**\_список MCI**</span><span class="sxs-lookup"><span data-stu-id="3c842-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="3c842-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c842-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

