---
title: Структура MCI_VD_PLAY_PARMS (МЦиапи. h)
description: Структура MCI \_ VD \_ Play \_ пармс содержит сведения о положении и скорости для команды MCI \_ Play для устройств видеодиск.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071666"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="40b34-104">\_Структура MCI VD \_ Play \_ пармс</span><span class="sxs-lookup"><span data-stu-id="40b34-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="40b34-105">Структура **MCI \_ VD \_ Play \_ пармс** содержит сведения о положении и скорости для команды [**MCI \_ Play**](mci-play.md) для устройств видеодиск.</span><span class="sxs-lookup"><span data-stu-id="40b34-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b34-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40b34-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="40b34-107">Члены</span><span class="sxs-lookup"><span data-stu-id="40b34-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="40b34-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="40b34-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="40b34-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="40b34-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="40b34-110">**двфром**</span><span class="sxs-lookup"><span data-stu-id="40b34-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="40b34-111">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="40b34-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="40b34-112">**двто**</span><span class="sxs-lookup"><span data-stu-id="40b34-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="40b34-113">Расположение для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="40b34-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="40b34-114">**двспид**</span><span class="sxs-lookup"><span data-stu-id="40b34-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="40b34-115">Скорость воспроизведения в кадрах за секунду.</span><span class="sxs-lookup"><span data-stu-id="40b34-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40b34-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40b34-116">Remarks</span></span>

<span data-ttu-id="40b34-117">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="40b34-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="40b34-118">Вы можете использовать структуру [**MCI \_ Play \_ пармс**](mci-play-parms.md) , а не **MCI \_ VD \_ Play \_ пармс** , если вы не используете расширенные элементы данных.</span><span class="sxs-lookup"><span data-stu-id="40b34-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="40b34-119">Требования</span><span class="sxs-lookup"><span data-stu-id="40b34-119">Requirements</span></span>



| <span data-ttu-id="40b34-120">Требование</span><span class="sxs-lookup"><span data-stu-id="40b34-120">Requirement</span></span> | <span data-ttu-id="40b34-121">Значение</span><span class="sxs-lookup"><span data-stu-id="40b34-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40b34-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40b34-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40b34-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="40b34-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="40b34-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40b34-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40b34-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="40b34-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="40b34-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="40b34-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="40b34-127"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="40b34-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40b34-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40b34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b34-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="40b34-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="40b34-130">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="40b34-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="40b34-131">**\_Воспроизведение MCI**</span><span class="sxs-lookup"><span data-stu-id="40b34-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="40b34-132">**MCI \_ Play \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="40b34-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="40b34-133">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40b34-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

