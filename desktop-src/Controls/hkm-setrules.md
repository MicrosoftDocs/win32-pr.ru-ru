---
title: Сообщение HKM_SETRULES (Коммктрл. h)
description: Определяет недопустимые сочетания и сочетание модификатора по умолчанию для элемента управления горячего ключа.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Элементы управления Windows для HKM_SETRULES сообщений
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491187"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="9f78b-104">\_Сообщение ХКМ сетрулес</span><span class="sxs-lookup"><span data-stu-id="9f78b-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="9f78b-105">Определяет недопустимые сочетания и сочетание модификатора по умолчанию для элемента управления горячего ключа.</span><span class="sxs-lookup"><span data-stu-id="9f78b-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f78b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f78b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f78b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f78b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f78b-108">Массив флагов, задающих недопустимые сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="9f78b-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="9f78b-109">Этот параметр может быть сочетанием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9f78b-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="9f78b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9f78b-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="9f78b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9f78b-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="9f78b-112"><dt>**ХККОМБ \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="9f78b-113">ALT</span><span class="sxs-lookup"><span data-stu-id="9f78b-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="9f78b-114"><dt>**ХККОМБ \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="9f78b-115">CTRL</span><span class="sxs-lookup"><span data-stu-id="9f78b-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="9f78b-116"><dt>**\_ЦС хккомб**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="9f78b-117">CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="9f78b-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="9f78b-118"><dt>**ХККОМБ \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="9f78b-119">Неизмененные ключи</span><span class="sxs-lookup"><span data-stu-id="9f78b-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="9f78b-120"><dt>**ХККОМБ \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="9f78b-121">МЕСТИ</span><span class="sxs-lookup"><span data-stu-id="9f78b-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="9f78b-122"><dt>**ХККОМБ \_ SA**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="9f78b-123">SHIFT + ALT</span><span class="sxs-lookup"><span data-stu-id="9f78b-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="9f78b-124"><dt>**ХККОМБ \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="9f78b-125">SHIFT + CTRL</span><span class="sxs-lookup"><span data-stu-id="9f78b-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="9f78b-126"><dt>**ХККОМБ \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="9f78b-127">SHIFT + CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="9f78b-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="9f78b-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f78b-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f78b-129">Массив флагов, указывающих сочетание клавиш, которое будет использоваться при вводе пользователем недопустимого сочетания.</span><span class="sxs-lookup"><span data-stu-id="9f78b-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="9f78b-130">Список значений флагов модификаторов см. в описании сообщения ХКМ- [**\_ горячих клавиш**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="9f78b-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f78b-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f78b-131">Return value</span></span>

<span data-ttu-id="9f78b-132">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9f78b-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f78b-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f78b-133">Remarks</span></span>

<span data-ttu-id="9f78b-134">Когда пользователь вводит недопустимое сочетание клавиш, как определено флагами, указанными в параметре *wParam*, система использует оператор побитового или для объединения вводимых пользователем ключей с флагами, указанными в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="9f78b-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="9f78b-135">Полученное сочетание клавиш преобразуется в строку и затем отображается в элементе управления "горячая клавиша".</span><span class="sxs-lookup"><span data-stu-id="9f78b-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f78b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="9f78b-136">Requirements</span></span>



| <span data-ttu-id="9f78b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="9f78b-137">Requirement</span></span> | <span data-ttu-id="9f78b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9f78b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f78b-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f78b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9f78b-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f78b-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f78b-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f78b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9f78b-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f78b-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f78b-143">Header</span><span class="sxs-lookup"><span data-stu-id="9f78b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f78b-144"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f78b-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





