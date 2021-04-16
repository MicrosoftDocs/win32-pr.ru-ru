---
description: Имитирует ряд типизированных символов.
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: Метод TypeText класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684261"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="d53f5-103">Метод TypeText \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="d53f5-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="d53f5-104">Имитирует ряд типизированных символов.</span><span class="sxs-lookup"><span data-stu-id="d53f5-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="d53f5-105">Это эквивалентно вызову [**пресскэй**](presskey-msvm-keyboard.md) , за которым следует [**релеасекэй**](releasekey-msvm-keyboard.md) для каждого символа в строке.</span><span class="sxs-lookup"><span data-stu-id="d53f5-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d53f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d53f5-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="d53f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d53f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d53f5-108">*асЦиитекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d53f5-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d53f5-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="d53f5-109">Type: **string**</span></span>

<span data-ttu-id="d53f5-110">Последовательность символов ASCII или Юникода для ввода.</span><span class="sxs-lookup"><span data-stu-id="d53f5-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="d53f5-111">Максимальная длина этой строки зависит от типа символов в строке.</span><span class="sxs-lookup"><span data-stu-id="d53f5-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="d53f5-112">Тип строки</span><span class="sxs-lookup"><span data-stu-id="d53f5-112">String type</span></span>        | <span data-ttu-id="d53f5-113">Максимальное число символов</span><span class="sxs-lookup"><span data-stu-id="d53f5-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d53f5-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="d53f5-114">ASCII</span></span><br/>   | <span data-ttu-id="d53f5-115">512</span><span class="sxs-lookup"><span data-stu-id="d53f5-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="d53f5-116">Юникод</span><span class="sxs-lookup"><span data-stu-id="d53f5-116">Unicode</span></span><br/> | <span data-ttu-id="d53f5-117">256 – 512, в зависимости от количества суррогатных пар в строке.</span><span class="sxs-lookup"><span data-stu-id="d53f5-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d53f5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d53f5-118">Return value</span></span>

<span data-ttu-id="d53f5-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d53f5-119">Type: **uint32**</span></span>

<span data-ttu-id="d53f5-120">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="d53f5-120">A return value of zero indicates success.</span></span> <span data-ttu-id="d53f5-121">Возвращаемое значение, равное единице, указывает на сбой, вызванный непреобразованными символами во входной строке.</span><span class="sxs-lookup"><span data-stu-id="d53f5-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="d53f5-122">Все остальные ненулевые значения указывают на ошибку при изменении состояния ключа.</span><span class="sxs-lookup"><span data-stu-id="d53f5-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="d53f5-123">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d53f5-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d53f5-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-125">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d53f5-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-126">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d53f5-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-127">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d53f5-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-128">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d53f5-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-129">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d53f5-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-130">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d53f5-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-131">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d53f5-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-132">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d53f5-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-133">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d53f5-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-134">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d53f5-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d53f5-135">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d53f5-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d53f5-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d53f5-136">Remarks</span></span>

<span data-ttu-id="d53f5-137">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d53f5-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d53f5-138">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d53f5-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d53f5-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="d53f5-139">Examples</span></span>

<span data-ttu-id="d53f5-140">В следующем примере кода C# моделируется ввод текста.</span><span class="sxs-lookup"><span data-stu-id="d53f5-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="d53f5-141">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d53f5-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
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

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
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
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="d53f5-142">Следующий образец Visual Basic Scripting Edition (VBScript) моделирует ввод текста.</span><span class="sxs-lookup"><span data-stu-id="d53f5-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


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
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
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
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="d53f5-143">Требования</span><span class="sxs-lookup"><span data-stu-id="d53f5-143">Requirements</span></span>



| <span data-ttu-id="d53f5-144">Требование</span><span class="sxs-lookup"><span data-stu-id="d53f5-144">Requirement</span></span> | <span data-ttu-id="d53f5-145">Значение</span><span class="sxs-lookup"><span data-stu-id="d53f5-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53f5-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d53f5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d53f5-147">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d53f5-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d53f5-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d53f5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d53f5-149">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d53f5-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d53f5-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d53f5-150">Namespace</span></span><br/>                | <span data-ttu-id="d53f5-151">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d53f5-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d53f5-152">MOF</span><span class="sxs-lookup"><span data-stu-id="d53f5-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d53f5-153"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d53f5-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d53f5-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d53f5-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d53f5-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d53f5-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d53f5-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d53f5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53f5-157">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="d53f5-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

