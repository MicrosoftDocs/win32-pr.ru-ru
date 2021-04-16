---
description: '\_Структура байтов с меткой Определяет битовую пару с меткой. Метка БИТОВой пары с метками отображается при обнаружении определенного значения свойства Byte.'
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Структура LABELED_BYTE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650994"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="68bbc-104">\_Структура БАЙТОВ с меткой</span><span class="sxs-lookup"><span data-stu-id="68bbc-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="68bbc-105">Структура **\_ байтов с МЕТКОЙ** Определяет битовую пару с меткой.</span><span class="sxs-lookup"><span data-stu-id="68bbc-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="68bbc-106">**Метка** битовой пары с метками отображается при обнаружении определенного значения свойства Byte.</span><span class="sxs-lookup"><span data-stu-id="68bbc-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bbc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68bbc-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="68bbc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="68bbc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="68bbc-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68bbc-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="68bbc-110">БАЙТОВое значение свойства, которое необходимо обнаружить.</span><span class="sxs-lookup"><span data-stu-id="68bbc-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="68bbc-111">**Label**</span><span class="sxs-lookup"><span data-stu-id="68bbc-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="68bbc-112">Текстовое описание или метка, отображаемая при обнаружении значения, указанного в элементе **value** .</span><span class="sxs-lookup"><span data-stu-id="68bbc-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68bbc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68bbc-113">Remarks</span></span>

<span data-ttu-id="68bbc-114">Элемент **лплабеледбитетабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих один или несколько элементов **Label** в парах «байтовые значения».</span><span class="sxs-lookup"><span data-stu-id="68bbc-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="68bbc-115">Эти пары используются, если требуется отобразить метку вместо определенного БАЙТового значения, найденного в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="68bbc-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="68bbc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="68bbc-116">Requirements</span></span>



| <span data-ttu-id="68bbc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="68bbc-117">Requirement</span></span> | <span data-ttu-id="68bbc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="68bbc-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="68bbc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68bbc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68bbc-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68bbc-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="68bbc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68bbc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68bbc-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68bbc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="68bbc-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="68bbc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68bbc-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68bbc-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bbc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68bbc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bbc-126">SET</span><span class="sxs-lookup"><span data-stu-id="68bbc-126">SET</span></span>](set.md)
</dt> </dl>

 

 




