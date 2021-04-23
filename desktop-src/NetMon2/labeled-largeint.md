---
description: Структура с МЕТКОЙ \_ ларжеинт определяет метку, которая отображается при обнаружении определенного значения свойства ларжеинт.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Структура LABELED_LARGEINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080853"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="14705-103">\_Структура ЛАРЖЕИНТ с меткой</span><span class="sxs-lookup"><span data-stu-id="14705-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="14705-104">Структура с **меткой \_ ларжеинт** определяет метку, которая отображается при обнаружении определенного значения свойства ларжеинт.</span><span class="sxs-lookup"><span data-stu-id="14705-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="14705-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14705-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="14705-106">Члены</span><span class="sxs-lookup"><span data-stu-id="14705-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="14705-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="14705-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="14705-108">ЛАРЖЕИНТ значение свойства, которое необходимо обнаружить.</span><span class="sxs-lookup"><span data-stu-id="14705-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="14705-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="14705-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="14705-110">Текстовое описание или метка, отображаемая при обнаружении значения ЛАРЖЕИНТ, указанного в элементе **value** .</span><span class="sxs-lookup"><span data-stu-id="14705-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14705-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14705-111">Remarks</span></span>

<span data-ttu-id="14705-112">Элемент **лплабеледларжеинттабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих один или несколько элементов **Label** в парах значений ларжеинт.</span><span class="sxs-lookup"><span data-stu-id="14705-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="14705-113">Эти пары используются, если требуется отобразить метку вместо определенного значения ЛАРЖЕИНТ, которое находится в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="14705-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="14705-114">Требования</span><span class="sxs-lookup"><span data-stu-id="14705-114">Requirements</span></span>



| <span data-ttu-id="14705-115">Требование</span><span class="sxs-lookup"><span data-stu-id="14705-115">Requirement</span></span> | <span data-ttu-id="14705-116">Значение</span><span class="sxs-lookup"><span data-stu-id="14705-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14705-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14705-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14705-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14705-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="14705-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14705-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14705-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14705-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="14705-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14705-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14705-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14705-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14705-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14705-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14705-124">SET</span><span class="sxs-lookup"><span data-stu-id="14705-124">SET</span></span>](set.md)
</dt> </dl>

 

 




