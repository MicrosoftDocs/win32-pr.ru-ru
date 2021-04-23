---
title: Перечисление TITLEBAR_TYPE (Софткбдк. h)
description: Элементы перечисления типа "строка заголовка" \_ используются для указания типов титлебарс, доступных для окна с экранной клавиатурой.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Платформа текстовых служб для перечисления TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681896"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="c48db-104">Перечисление типов в строке заголовка \_</span><span class="sxs-lookup"><span data-stu-id="c48db-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="c48db-105">Элементы перечисления **\_ типа "строка заголовка** " используются для указания типов титлебарс, доступных для окна с экранной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="c48db-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48db-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c48db-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c48db-107">Константы</span><span class="sxs-lookup"><span data-stu-id="c48db-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c48db-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**\_без заголовка**</span><span class="sxs-lookup"><span data-stu-id="c48db-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="c48db-109">В окне экранной клавиатуры не используется заголовок.</span><span class="sxs-lookup"><span data-stu-id="c48db-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="c48db-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**Захват окна "заголовок по \_ \_ горизонтали" \_**</span><span class="sxs-lookup"><span data-stu-id="c48db-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="c48db-111">В окне экранной клавиатуры используется только горизонтальная панель захвата.</span><span class="sxs-lookup"><span data-stu-id="c48db-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="c48db-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**\_захват заголовка окна \_ верти \_ только**</span><span class="sxs-lookup"><span data-stu-id="c48db-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="c48db-113">В окне экранной клавиатуры используется только вертикальная панель захвата.</span><span class="sxs-lookup"><span data-stu-id="c48db-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="c48db-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**\_кнопка захвата в строке заголовка \_**</span><span class="sxs-lookup"><span data-stu-id="c48db-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="c48db-115">В окне экранной клавиатуры используется только кнопка захвата.</span><span class="sxs-lookup"><span data-stu-id="c48db-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c48db-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c48db-116">Requirements</span></span>



| <span data-ttu-id="c48db-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c48db-117">Requirement</span></span> | <span data-ttu-id="c48db-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c48db-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c48db-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c48db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c48db-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c48db-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c48db-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c48db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c48db-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c48db-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c48db-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c48db-123">Redistributable</span></span><br/>          | <span data-ttu-id="c48db-124">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="c48db-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c48db-125">Header</span><span class="sxs-lookup"><span data-stu-id="c48db-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c48db-126"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c48db-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c48db-127">IDL</span><span class="sxs-lookup"><span data-stu-id="c48db-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c48db-128"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c48db-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





