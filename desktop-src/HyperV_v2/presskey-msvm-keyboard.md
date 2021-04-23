---
description: Имитирует нажатие клавиши.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Метод Пресскэй класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664680"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="4c522-103">Метод Пресскэй \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="4c522-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="4c522-104">Имитирует нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="4c522-104">Simulates a key press.</span></span> <span data-ttu-id="4c522-105">При успешном выполнении ключ будет находиться в неправильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4c522-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c522-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c522-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="4c522-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c522-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c522-108">*keyCode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c522-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c522-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c522-109">Type: **uint32**</span></span>

<span data-ttu-id="4c522-110">Код виртуального ключа для нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="4c522-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="4c522-111">Список кодов виртуальных клавиш см. в разделе [**коды виртуальных**](../inputdev/virtual-key-codes.md)клавиш.</span><span class="sxs-lookup"><span data-stu-id="4c522-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c522-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c522-112">Return value</span></span>

<span data-ttu-id="4c522-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c522-113">Type: **uint32**</span></span>

<span data-ttu-id="4c522-114">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="4c522-114">A return value of zero indicates success.</span></span> <span data-ttu-id="4c522-115">Ненулевое значение указывает на ошибку при изменении состояния ключа.</span><span class="sxs-lookup"><span data-stu-id="4c522-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="4c522-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4c522-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4c522-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="4c522-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="4c522-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="4c522-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="4c522-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="4c522-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="4c522-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="4c522-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="4c522-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="4c522-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="4c522-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4c522-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="4c522-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4c522-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c522-129">Remarks</span></span>

<span data-ttu-id="4c522-130">Метод **пресскэй** сопоставляет ссылки на **\_ меню VK** (18), **VK \_ Control** (17) и **VK \_ SHIFT** (16) с **VK \_ лмену** (164), **VK \_ Лконтрол** (162) и **VK \_ лшифт** (160), соответственно, так как **\_ меню VK**, **VK \_ Control** и **VK \_ SHIFT** , не являются реальными ключами на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="4c522-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="4c522-131">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4c522-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4c522-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4c522-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4c522-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="4c522-133">Examples</span></span>

<span data-ttu-id="4c522-134">В следующем примере кода C# имитируется нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="4c522-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="4c522-135">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="4c522-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



<span data-ttu-id="4c522-136">Следующий пример Visual Basic Scripting Edition (VBScript) имитирует нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="4c522-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


```VB
option explicit 

dim objWMIService
dim fileSystem
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="4c522-137">Требования</span><span class="sxs-lookup"><span data-stu-id="4c522-137">Requirements</span></span>



| <span data-ttu-id="4c522-138">Требование</span><span class="sxs-lookup"><span data-stu-id="4c522-138">Requirement</span></span> | <span data-ttu-id="4c522-139">Значение</span><span class="sxs-lookup"><span data-stu-id="4c522-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c522-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c522-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4c522-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4c522-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4c522-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c522-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4c522-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4c522-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c522-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c522-144">Namespace</span></span><br/>                | <span data-ttu-id="4c522-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4c522-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4c522-146">MOF</span><span class="sxs-lookup"><span data-stu-id="4c522-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c522-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c522-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c522-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4c522-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c522-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c522-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4c522-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c522-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c522-151">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="4c522-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="4c522-152">**Коды виртуальных клавиш**</span><span class="sxs-lookup"><span data-stu-id="4c522-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

