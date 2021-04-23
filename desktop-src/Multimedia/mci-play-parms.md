---
title: Структура MCI_PLAY_PARMS (МЦиапи. h)
description: Структура MCI \_ Play \_ пармс содержит сведения о размещении для \_ команды MCI Play.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- MCI_PLAY_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988176"
---
# <a name="mci_play_parms-structure"></a><span data-ttu-id="95a8c-104">\_Структура MCI Play \_ пармс</span><span class="sxs-lookup"><span data-stu-id="95a8c-104">MCI\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="95a8c-105">Структура **MCI \_ Play \_ пармс** содержит сведения о размещении для команды [**MCI \_ Play**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="95a8c-105">The **MCI\_PLAY\_PARMS** structure contains positioning information for the [**MCI\_PLAY**](mci-play.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a8c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95a8c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="95a8c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="95a8c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="95a8c-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="95a8c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="95a8c-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="95a8c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="95a8c-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="95a8c-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="95a8c-111">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="95a8c-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="95a8c-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="95a8c-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="95a8c-113">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="95a8c-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95a8c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95a8c-114">Remarks</span></span>

<span data-ttu-id="95a8c-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="95a8c-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a8c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="95a8c-116">Requirements</span></span>



| <span data-ttu-id="95a8c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="95a8c-117">Requirement</span></span> | <span data-ttu-id="95a8c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="95a8c-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="95a8c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95a8c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95a8c-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95a8c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="95a8c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95a8c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95a8c-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="95a8c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="95a8c-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="95a8c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95a8c-124"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a8c-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a8c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95a8c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a8c-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="95a8c-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="95a8c-127">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="95a8c-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="95a8c-128">**\_Воспроизведение MCI**</span><span class="sxs-lookup"><span data-stu-id="95a8c-128">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="95a8c-129">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95a8c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

