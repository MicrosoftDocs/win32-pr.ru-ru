---
title: Константы TF_MOD_ (Мсктф. h)
description: '\_ \_ Константы TF mod \ указывают модификаторы ключа в структуре TF \_ пресерведкэй.'
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071585"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="da9bf-103">TF \_ Mod \_ \* константы</span><span class="sxs-lookup"><span data-stu-id="da9bf-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="da9bf-104">\_ \_ \* Константы TF mod указывают модификаторы ключа в структуре [tf \_ пресерведкэй](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .</span><span class="sxs-lookup"><span data-stu-id="da9bf-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="da9bf-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="da9bf-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="da9bf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="da9bf-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="da9bf-107"><dt>**Tf \_ MOD \_ ALT**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="da9bf-108">Нажата одна из клавиш ALT</span><span class="sxs-lookup"><span data-stu-id="da9bf-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="da9bf-109"><dt>**Tf \_ 0x0002 \_ элемента управления mod**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="da9bf-110">Нажата любая из клавиш CTRL</span><span class="sxs-lookup"><span data-stu-id="da9bf-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="da9bf-111"><dt>**Tf \_ 0x0004 \_ сдвиг mod**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="da9bf-112">Нажата любая из клавиш SHIFT</span><span class="sxs-lookup"><span data-stu-id="da9bf-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="da9bf-113"><dt>**Tf \_ MOD \_ ралт**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="da9bf-114">Нажата правая клавиша ALT</span><span class="sxs-lookup"><span data-stu-id="da9bf-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="da9bf-115"><dt>**Tf \_ MOD \_ рконтрол**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="da9bf-116">Нажата правая клавиша CTRL</span><span class="sxs-lookup"><span data-stu-id="da9bf-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="da9bf-117"><dt>**Tf \_ MOD \_ ршифт**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="da9bf-118">Нажата клавиша SHIFT справа</span><span class="sxs-lookup"><span data-stu-id="da9bf-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="da9bf-119"><dt>**Tf \_ MOD \_ лалт**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="da9bf-120">Нажата левая клавиша ALT</span><span class="sxs-lookup"><span data-stu-id="da9bf-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="da9bf-121"><dt>**Tf \_ MOD \_ лконтрол**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="da9bf-122">Нажата левая клавиша CTRL</span><span class="sxs-lookup"><span data-stu-id="da9bf-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="da9bf-123"><dt>**Tf \_ MOD \_ лшифт**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="da9bf-124">Нажата клавиша SHIFT слева</span><span class="sxs-lookup"><span data-stu-id="da9bf-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="da9bf-125"><dt>**Tf \_ MOD \_ для \_ KEYUP**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="da9bf-126">Событие будет запущено при освобождении ключа.</span><span class="sxs-lookup"><span data-stu-id="da9bf-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="da9bf-127">Без этого флага событие срабатывает при нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="da9bf-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="da9bf-128"><dt>**Tf \_ 0x0400 \_ пропуск \_ всех \_ модификаторов mod**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="da9bf-129">Состояние клавиш ALT, CTRL и SHIFT игнорируется.</span><span class="sxs-lookup"><span data-stu-id="da9bf-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="da9bf-130">Это означает, что событие будет срабатывать при нажатии на виртуальный ключ независимо от того, какие клавиши-модификаторы нажаты.</span><span class="sxs-lookup"><span data-stu-id="da9bf-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="da9bf-131">Требования</span><span class="sxs-lookup"><span data-stu-id="da9bf-131">Requirements</span></span>



| <span data-ttu-id="da9bf-132">Требование</span><span class="sxs-lookup"><span data-stu-id="da9bf-132">Requirement</span></span> | <span data-ttu-id="da9bf-133">Значение</span><span class="sxs-lookup"><span data-stu-id="da9bf-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da9bf-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da9bf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="da9bf-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="da9bf-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="da9bf-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da9bf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="da9bf-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="da9bf-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="da9bf-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="da9bf-138">Redistributable</span></span><br/>          | <span data-ttu-id="da9bf-139">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="da9bf-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="da9bf-140">Header</span><span class="sxs-lookup"><span data-stu-id="da9bf-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="da9bf-141"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="da9bf-142">IDL</span><span class="sxs-lookup"><span data-stu-id="da9bf-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da9bf-143"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da9bf-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9bf-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da9bf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9bf-145">TF \_ пресерведкэй</span><span class="sxs-lookup"><span data-stu-id="da9bf-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





