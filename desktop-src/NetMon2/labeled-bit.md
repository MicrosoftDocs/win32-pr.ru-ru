---
description: '\_Битовая структура с меткой Определяет битовую пару меток.'
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Структура LABELED_BIT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650570"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="708db-103">\_Битовая структура с меткой</span><span class="sxs-lookup"><span data-stu-id="708db-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="708db-104">**\_ Битовая** структура с меткой Определяет битовую пару меток.</span><span class="sxs-lookup"><span data-stu-id="708db-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="708db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="708db-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="708db-106">Члены</span><span class="sxs-lookup"><span data-stu-id="708db-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="708db-107">**битнумбер**</span><span class="sxs-lookup"><span data-stu-id="708db-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="708db-108">РАЗРЯДное число БИТОВой пары меток.</span><span class="sxs-lookup"><span data-stu-id="708db-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="708db-109">Диапазон значений — от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="708db-109">Values range from 0 to 255.</span></span> <span data-ttu-id="708db-110">Установите для элемента **БИТНУМБЕР** бит, используемый при сравнении значения свойства.</span><span class="sxs-lookup"><span data-stu-id="708db-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="708db-111">**лабелофф**</span><span class="sxs-lookup"><span data-stu-id="708db-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="708db-112">Строка или метка, отображаемая, если бит, указанный в **битнумбер** , равен нулю.</span><span class="sxs-lookup"><span data-stu-id="708db-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="708db-113">Например, возможной меткой является "бит OFF".</span><span class="sxs-lookup"><span data-stu-id="708db-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="708db-114">**лабелон**</span><span class="sxs-lookup"><span data-stu-id="708db-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="708db-115">Строка или метка, отображаемая, если бит, указанный в **битнумбер** , равен 1.</span><span class="sxs-lookup"><span data-stu-id="708db-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="708db-116">Например, возможна метка "bit ON".</span><span class="sxs-lookup"><span data-stu-id="708db-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="708db-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="708db-117">Remarks</span></span>

<span data-ttu-id="708db-118">Массив **\_ битовых структур с метками** используется для определения набора пар битов меток.</span><span class="sxs-lookup"><span data-stu-id="708db-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="708db-119">Указатель на массив указывается в элементе **лплабеледбит** структуры [набора](set.md) .</span><span class="sxs-lookup"><span data-stu-id="708db-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="708db-120">Эти пары используются, если требуется отобразить метку на основе параметра каждого бита.</span><span class="sxs-lookup"><span data-stu-id="708db-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="708db-121">Как правило, этот тип набора используется для указания значения битов (ON или OFF).</span><span class="sxs-lookup"><span data-stu-id="708db-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="708db-122">Если задан бит BIT, сетевой монитор отображает только биты, включенные в массив **набора** структур.</span><span class="sxs-lookup"><span data-stu-id="708db-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="708db-123">Биты, которые не находятся в структуре **набора** , не отображаются.</span><span class="sxs-lookup"><span data-stu-id="708db-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="708db-124">Требования</span><span class="sxs-lookup"><span data-stu-id="708db-124">Requirements</span></span>



| <span data-ttu-id="708db-125">Требование</span><span class="sxs-lookup"><span data-stu-id="708db-125">Requirement</span></span> | <span data-ttu-id="708db-126">Значение</span><span class="sxs-lookup"><span data-stu-id="708db-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="708db-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="708db-127">Minimum supported client</span></span><br/> | <span data-ttu-id="708db-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="708db-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="708db-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="708db-129">Minimum supported server</span></span><br/> | <span data-ttu-id="708db-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="708db-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="708db-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="708db-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="708db-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="708db-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="708db-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="708db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708db-134">SET</span><span class="sxs-lookup"><span data-stu-id="708db-134">SET</span></span>](set.md)
</dt> </dl>

 

 




