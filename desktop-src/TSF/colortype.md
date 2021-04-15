---
title: Перечисление КОЛОРТИПЕ (Софткбдк. h)
description: Элементы перечисления КОЛОРТИПЕ используются для указания типов цветов, доступных для экранной клавиатуры.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Платформа текстовых служб перечисления КОЛОРТИПЕ
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661949"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="c27aa-104">Перечисление КОЛОРТИПЕ</span><span class="sxs-lookup"><span data-stu-id="c27aa-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="c27aa-105">Элементы перечисления **колортипе** используются для указания типов цветов, доступных для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="c27aa-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27aa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c27aa-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="c27aa-107">Константы</span><span class="sxs-lookup"><span data-stu-id="c27aa-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c27aa-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**бкколор**</span><span class="sxs-lookup"><span data-stu-id="c27aa-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="c27aa-109">Цвет фона.</span><span class="sxs-lookup"><span data-stu-id="c27aa-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="c27aa-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**унселфореколор**</span><span class="sxs-lookup"><span data-stu-id="c27aa-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="c27aa-111">Цвет переднего плана не выбран.</span><span class="sxs-lookup"><span data-stu-id="c27aa-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="c27aa-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**унселтекстколор**</span><span class="sxs-lookup"><span data-stu-id="c27aa-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="c27aa-113">Цвет невыделенного текста.</span><span class="sxs-lookup"><span data-stu-id="c27aa-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="c27aa-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**селфореколор**</span><span class="sxs-lookup"><span data-stu-id="c27aa-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="c27aa-115">Выбранный цвет переднего плана.</span><span class="sxs-lookup"><span data-stu-id="c27aa-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="c27aa-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**селтекстколор**</span><span class="sxs-lookup"><span data-stu-id="c27aa-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="c27aa-117">Цвет выбранного текста.</span><span class="sxs-lookup"><span data-stu-id="c27aa-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="c27aa-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Максимальный \_ \_ Тип цвета**</span><span class="sxs-lookup"><span data-stu-id="c27aa-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="c27aa-119">Максимальный тип цвета.</span><span class="sxs-lookup"><span data-stu-id="c27aa-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c27aa-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c27aa-120">Requirements</span></span>



| <span data-ttu-id="c27aa-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c27aa-121">Requirement</span></span> | <span data-ttu-id="c27aa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c27aa-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c27aa-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c27aa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c27aa-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c27aa-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c27aa-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c27aa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c27aa-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c27aa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c27aa-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c27aa-127">Redistributable</span></span><br/>          | <span data-ttu-id="c27aa-128">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="c27aa-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c27aa-129">Header</span><span class="sxs-lookup"><span data-stu-id="c27aa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c27aa-130"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c27aa-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c27aa-131">IDL</span><span class="sxs-lookup"><span data-stu-id="c27aa-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c27aa-132"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c27aa-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





