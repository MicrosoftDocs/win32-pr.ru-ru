---
description: '\_Структура SYSTEMTIME с меткой не определяет метку, которая отображается при обнаружении определенного значения свойства SYSTEMTIME.'
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Структура LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913444"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="01aef-103">\_Структура SYSTEMTIME с меткой</span><span class="sxs-lookup"><span data-stu-id="01aef-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="01aef-104">Структура **\_ SYSTEMTIME с меткой** не определяет метку, которая отображается при обнаружении определенного значения свойства SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="01aef-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="01aef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01aef-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="01aef-106">Члены</span><span class="sxs-lookup"><span data-stu-id="01aef-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="01aef-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="01aef-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="01aef-108">Значение SYSTEMTIME для свойства, которое необходимо обнаружить.</span><span class="sxs-lookup"><span data-stu-id="01aef-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="01aef-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="01aef-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="01aef-110">Текстовое описание или метка, отображаемая при обнаружении значения SYSTEMTIME, указанного в элементе **value** .</span><span class="sxs-lookup"><span data-stu-id="01aef-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01aef-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01aef-111">Remarks</span></span>

<span data-ttu-id="01aef-112">Элемент **лплабеледсистемтиметабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих одну или несколько пар значений меток.</span><span class="sxs-lookup"><span data-stu-id="01aef-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="01aef-113">Эти пары используются, если требуется отобразить метку вместо определенного значения ЛАРЖЕИНТ, найденного в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="01aef-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="01aef-114">Требования</span><span class="sxs-lookup"><span data-stu-id="01aef-114">Requirements</span></span>



| <span data-ttu-id="01aef-115">Требование</span><span class="sxs-lookup"><span data-stu-id="01aef-115">Requirement</span></span> | <span data-ttu-id="01aef-116">Значение</span><span class="sxs-lookup"><span data-stu-id="01aef-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01aef-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01aef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="01aef-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01aef-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="01aef-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01aef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="01aef-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="01aef-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01aef-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="01aef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="01aef-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="01aef-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01aef-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01aef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01aef-124">SET</span><span class="sxs-lookup"><span data-stu-id="01aef-124">SET</span></span>](set.md)
</dt> </dl>

 

 




