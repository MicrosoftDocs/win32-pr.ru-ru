---
title: Структура MCI_BREAK_PARMS (МЦиапи. h)
description: '\_Структура пармс разрывов MCI \_ содержит код виртуального ключа и сведения о окне для команды MCI \_ break.'
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534016"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="0f3ef-104">\_Структура MCI Break \_ пармс</span><span class="sxs-lookup"><span data-stu-id="0f3ef-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="0f3ef-105">Структура **\_ \_ Пармс разрывов MCI** содержит код виртуального ключа и сведения о окне для команды [**MCI \_ break**](mci-break.md) .</span><span class="sxs-lookup"><span data-stu-id="0f3ef-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3ef-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f3ef-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="0f3ef-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0f3ef-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f3ef-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="0f3ef-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0f3ef-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0f3ef-110">**нвирткэй**</span><span class="sxs-lookup"><span data-stu-id="0f3ef-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="0f3ef-111">Код виртуального ключа для ключа разрыва.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="0f3ef-112">**хвндбреак**</span><span class="sxs-lookup"><span data-stu-id="0f3ef-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="0f3ef-113">Обработчик для окна, который должен быть текущим окном для обнаружения прерываний.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f3ef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f3ef-114">Remarks</span></span>

<span data-ttu-id="0f3ef-115">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="0f3ef-116">Определены следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0f3ef-116">The following flags are defined:</span></span>

<span data-ttu-id="0f3ef-117">\_HWND разрыва MCI \_</span><span class="sxs-lookup"><span data-stu-id="0f3ef-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="0f3ef-118">Проверяет элемент **хвндбреак** , указывающий окно, которое должно иметь фокус на включение обнаружения прерываний.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="0f3ef-119">\_ключ разрыва MCI \_</span><span class="sxs-lookup"><span data-stu-id="0f3ef-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="0f3ef-120">Проверяет элемент **нвирткэй** , указывающий на код виртуального ключа, который будет использоваться для ключа разрыва.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="0f3ef-121">\_разрыв MCI \_ отключен</span><span class="sxs-lookup"><span data-stu-id="0f3ef-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="0f3ef-122">Отключает любой существующий ключ разрыва.</span><span class="sxs-lookup"><span data-stu-id="0f3ef-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3ef-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0f3ef-123">Requirements</span></span>



| <span data-ttu-id="0f3ef-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0f3ef-124">Requirement</span></span> | <span data-ttu-id="0f3ef-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0f3ef-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3ef-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f3ef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3ef-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f3ef-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f3ef-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f3ef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3ef-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f3ef-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f3ef-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f3ef-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3ef-131"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3ef-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f3ef-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f3ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3ef-133">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0f3ef-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0f3ef-134">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="0f3ef-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0f3ef-135">**\_разрыв MCI**</span><span class="sxs-lookup"><span data-stu-id="0f3ef-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="0f3ef-136">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f3ef-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

