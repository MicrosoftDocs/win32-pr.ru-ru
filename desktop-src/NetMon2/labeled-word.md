---
description: Структура слова с МЕТКАми \_ определяет метку, которая отображается при обнаружении определенного значения свойства Word.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Структура LABELED_WORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674085"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="b4046-103">Структура слова с МЕТКАми \_</span><span class="sxs-lookup"><span data-stu-id="b4046-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="b4046-104">Структура **\_ слова с метками** определяет метку, которая отображается при обнаружении определенного значения свойства Word.</span><span class="sxs-lookup"><span data-stu-id="b4046-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4046-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4046-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="b4046-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b4046-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4046-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b4046-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="b4046-108">Значение слова для свойства, которое необходимо обнаружить.</span><span class="sxs-lookup"><span data-stu-id="b4046-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="b4046-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="b4046-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="b4046-110">Текстовое описание или метка, отображаемая при обнаружении значения слова, указанного в элементе **value** .</span><span class="sxs-lookup"><span data-stu-id="b4046-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4046-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4046-111">Remarks</span></span>

<span data-ttu-id="b4046-112">Элемент **лплабеледвордтабле** структуры [Set](set.md) указывает на массив наборов структур, определяющих одну или несколько пар значений меток.</span><span class="sxs-lookup"><span data-stu-id="b4046-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="b4046-113">Эти пары используются, если требуется отобразить метку вместо определенного значения слова, которое найдено в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="b4046-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4046-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b4046-114">Requirements</span></span>



| <span data-ttu-id="b4046-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b4046-115">Requirement</span></span> | <span data-ttu-id="b4046-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b4046-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4046-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4046-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4046-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4046-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b4046-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4046-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4046-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4046-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b4046-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b4046-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4046-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4046-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4046-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4046-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4046-124">SET</span><span class="sxs-lookup"><span data-stu-id="b4046-124">SET</span></span>](set.md)
</dt> </dl>

 

 




