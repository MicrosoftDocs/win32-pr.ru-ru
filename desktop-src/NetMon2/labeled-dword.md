---
description: '\_Структура DWORD с меткой определяет метку, которая отображается при обнаружении определенного значения свойства DWORD.'
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Структура LABELED_DWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265650"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="f9b16-103">\_Структура DWORD с меткой</span><span class="sxs-lookup"><span data-stu-id="f9b16-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="f9b16-104">Структура **\_ DWORD с меткой** определяет метку, которая отображается при обнаружении определенного значения свойства DWORD.</span><span class="sxs-lookup"><span data-stu-id="f9b16-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9b16-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="f9b16-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f9b16-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9b16-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f9b16-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="f9b16-108">Значение DWORD свойства, которое необходимо обнаружить.</span><span class="sxs-lookup"><span data-stu-id="f9b16-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="f9b16-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="f9b16-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="f9b16-110">Текстовое описание или метка, отображаемая при обнаружении значения DWORD, указанного в элементе **value** .</span><span class="sxs-lookup"><span data-stu-id="f9b16-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9b16-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9b16-111">Remarks</span></span>

<span data-ttu-id="f9b16-112">Элемент **лплабеледдвордтабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих один или несколько элементов **Label** в парах значений DWORD.</span><span class="sxs-lookup"><span data-stu-id="f9b16-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="f9b16-113">Эти пары используются, если требуется отобразить метку вместо определенного значения DWORD, найденного в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="f9b16-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b16-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f9b16-114">Requirements</span></span>



| <span data-ttu-id="f9b16-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f9b16-115">Requirement</span></span> | <span data-ttu-id="f9b16-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f9b16-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b16-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9b16-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b16-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9b16-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f9b16-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9b16-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b16-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9b16-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f9b16-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f9b16-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9b16-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b16-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b16-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9b16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b16-124">SET</span><span class="sxs-lookup"><span data-stu-id="f9b16-124">SET</span></span>](set.md)
</dt> </dl>

 

 




