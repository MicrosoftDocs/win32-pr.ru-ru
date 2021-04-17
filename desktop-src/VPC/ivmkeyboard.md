---
title: Интерфейс Ивмкэйбоард (Впккоминтерфацес. h)
description: Управляет устройством клавиатуры в виртуальной машине. Ивмкэйбоард для виртуальной машины можно получить с помощью свойства клавиатуры Ивмвиртуалмачине.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Виртуальный ПК с интерфейсом Ивмкэйбоард
- Ивмкэйбоард интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691948"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="e179e-106">Интерфейс Ивмкэйбоард</span><span class="sxs-lookup"><span data-stu-id="e179e-106">IVMKeyboard interface</span></span>

<span data-ttu-id="e179e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e179e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e179e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e179e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e179e-109">Управляет устройством клавиатуры в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e179e-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="e179e-110">**Ивмкэйбоард** для виртуальной машины можно получить с помощью свойства [**Ивмвиртуалмачине:: Keyboard**](ivmvirtualmachine-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="e179e-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="e179e-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="e179e-111">Members</span></span>

<span data-ttu-id="e179e-112">Интерфейс **ивмкэйбоард** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e179e-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e179e-113">**Ивмкэйбоард** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e179e-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="e179e-114">Методы</span><span class="sxs-lookup"><span data-stu-id="e179e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e179e-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e179e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e179e-116">Методы</span><span class="sxs-lookup"><span data-stu-id="e179e-116">Methods</span></span>

<span data-ttu-id="e179e-117">Интерфейс **ивмкэйбоард** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e179e-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="e179e-118">Метод</span><span class="sxs-lookup"><span data-stu-id="e179e-118">Method</span></span>                                                       | <span data-ttu-id="e179e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e179e-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="e179e-120">**Нажимает**</span><span class="sxs-lookup"><span data-stu-id="e179e-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="e179e-121">Определяет, является ли указанный ключ недоступным.</span><span class="sxs-lookup"><span data-stu-id="e179e-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="e179e-122">**прессандрелеасекэй**</span><span class="sxs-lookup"><span data-stu-id="e179e-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="e179e-123">Имитирует нажатое клавиша, а затем освобождается.</span><span class="sxs-lookup"><span data-stu-id="e179e-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="e179e-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="e179e-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="e179e-125">Имитирует нажатой клавиша.</span><span class="sxs-lookup"><span data-stu-id="e179e-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="e179e-126">**релеасекэй**</span><span class="sxs-lookup"><span data-stu-id="e179e-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="e179e-127">Имитирует освобождение ключа.</span><span class="sxs-lookup"><span data-stu-id="e179e-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="e179e-128">**типеасЦиитекст**</span><span class="sxs-lookup"><span data-stu-id="e179e-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="e179e-129">Имитирует ряд вводимых в гостевой системе ключей ASCII.</span><span class="sxs-lookup"><span data-stu-id="e179e-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="e179e-130">**типекэйсекуенце**</span><span class="sxs-lookup"><span data-stu-id="e179e-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="e179e-131">Имитирует разделенный запятыми список ключей, вводимых в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="e179e-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e179e-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="e179e-132">Properties</span></span>

<span data-ttu-id="e179e-133">Интерфейс **ивмкэйбоард** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e179e-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="e179e-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="e179e-134">Property</span></span>                                                                | <span data-ttu-id="e179e-135">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e179e-135">Access type</span></span>           | <span data-ttu-id="e179e-136">Описание</span><span class="sxs-lookup"><span data-stu-id="e179e-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e179e-137">**хасексклусивеакцесс**</span><span class="sxs-lookup"><span data-stu-id="e179e-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="e179e-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e179e-138">Read/write</span></span><br/> | <span data-ttu-id="e179e-139">Указывает, имеет ли этот объект исключительный контроль над устройством клавиатуры виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e179e-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e179e-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e179e-140">Remarks</span></span>

<span data-ttu-id="e179e-141">Ключи можно ввести в виртуальную машину несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="e179e-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="e179e-142">Чтобы ввести обычную последовательность символов ASCII, используйте метод [**типеасЦиитекст**](ivmkeyboard-typeasciitext.md) .</span><span class="sxs-lookup"><span data-stu-id="e179e-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="e179e-143">Если требуется больше гибкости, **ивмкэйбоард** имеет несколько методов, предназначенных для использования с кодами клавиш, приведенными в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="e179e-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="e179e-144">Метод [**типекэйсекуенце**](ivmkeyboard-typekeysequence.md) может принимать разделенную запятыми строку кодов клавиш, которая будет нажата и отпущена в пределах виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e179e-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="e179e-145">Помимо этих кодов клавиш, ключевые слова можно использовать для принудительного нажатия клавиши или только для освобождения.</span><span class="sxs-lookup"><span data-stu-id="e179e-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="e179e-146">Ключевые слова UP и DOWN применяются только к коду ключа, непосредственно следующему за ключевым словом.</span><span class="sxs-lookup"><span data-stu-id="e179e-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="e179e-147">Чтобы избежать одновременной попытки доступа нескольких сценариев, приложений или пользователей к одному и тому же устройству клавиатуры, задайте для свойства [**Хасексклусивеакцесс**](ivmkeyboard-hasexclusiveaccess.md) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e179e-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="e179e-148">Если один процесс получает монопольный доступ, любые попытки других процессов отправить входные данные на устройство клавиатуры будут проигнорированы до тех пор, пока не будет освобожден монопольный доступ.</span><span class="sxs-lookup"><span data-stu-id="e179e-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="e179e-149">Требования</span><span class="sxs-lookup"><span data-stu-id="e179e-149">Requirements</span></span>



| <span data-ttu-id="e179e-150">Требование</span><span class="sxs-lookup"><span data-stu-id="e179e-150">Requirement</span></span> | <span data-ttu-id="e179e-151">Значение</span><span class="sxs-lookup"><span data-stu-id="e179e-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e179e-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e179e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e179e-153">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e179e-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e179e-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e179e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e179e-155">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e179e-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e179e-156">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e179e-156">End of client support</span></span><br/>    | <span data-ttu-id="e179e-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e179e-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e179e-158">Продукт</span><span class="sxs-lookup"><span data-stu-id="e179e-158">Product</span></span><br/>                  | <span data-ttu-id="e179e-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e179e-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e179e-160">Header</span><span class="sxs-lookup"><span data-stu-id="e179e-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="e179e-161"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e179e-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e179e-162">IID</span><span class="sxs-lookup"><span data-stu-id="e179e-162">IID</span></span><br/>                      | <span data-ttu-id="e179e-163">IID \_ ивмкэйбоард определен как 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="e179e-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="e179e-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e179e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e179e-165">Интерфейсы виртуальных ПК Windows</span><span class="sxs-lookup"><span data-stu-id="e179e-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e179e-166">Последовательности ключей</span><span class="sxs-lookup"><span data-stu-id="e179e-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

