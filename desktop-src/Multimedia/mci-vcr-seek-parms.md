---
title: Структура MCI_VCR_SEEK_PARMS (видеомагнитофон. h)
description: '\_Структура пармс в видеомагнитофоне MCI \_ \_ содержит параметры для \_ команды MCI Seek для устройств записи видеокассет.'
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489897"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="bc9e5-104">\_ \_ Структура пармс в видеомагнитофоне MCI \_</span><span class="sxs-lookup"><span data-stu-id="bc9e5-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="bc9e5-105">Структура **\_ \_ \_ пармс в видеомагнитофоне MCI** содержит параметры для команды [**MCI \_ Seek**](mci-seek.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9e5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc9e5-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="bc9e5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="bc9e5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc9e5-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bc9e5-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bc9e5-110">**двто**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="bc9e5-111">Положение для поиска.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="bc9e5-112">**двмарк**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="bc9e5-113">Нумерованная метка для поиска.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="bc9e5-114">**дват**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="bc9e5-115">Время начала поиска.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc9e5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc9e5-116">Remarks</span></span>

<span data-ttu-id="bc9e5-117">Позиции указываются в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="bc9e5-118">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="bc9e5-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9e5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bc9e5-119">Requirements</span></span>



| <span data-ttu-id="bc9e5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bc9e5-120">Requirement</span></span> | <span data-ttu-id="bc9e5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bc9e5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bc9e5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc9e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9e5-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc9e5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bc9e5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc9e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9e5-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc9e5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bc9e5-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bc9e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc9e5-127"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc9e5-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc9e5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc9e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc9e5-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc9e5-130">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bc9e5-131">**\_Поиск MCI**</span><span class="sxs-lookup"><span data-stu-id="bc9e5-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="bc9e5-132">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc9e5-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

