---
description: Можно скрыть кнопку Отмена, которая используется для отмены установки, с помощью параметра командной строки, установщик Windows API или настраиваемого действия. Кнопка Отмена может быть скрыта для части или всей установки в зависимости от используемого метода.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Скрытие кнопки "Отмена" во время установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650939"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="fe25d-104">Скрытие кнопки "Отмена" во время установки</span><span class="sxs-lookup"><span data-stu-id="fe25d-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="fe25d-105">Можно скрыть кнопку **Отмена** , которая используется для отмены установки, с помощью параметра командной строки, установщик Windows API или настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="fe25d-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="fe25d-106">Кнопка **Отмена** может быть скрыта для части или всей установки в зависимости от используемого метода.</span><span class="sxs-lookup"><span data-stu-id="fe25d-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="fe25d-107">Скрытие кнопки "Отмена" из командной строки</span><span class="sxs-lookup"><span data-stu-id="fe25d-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="fe25d-108">Во время установки кнопка **Отмена** может быть скрыта с помощью параметра командной строки (!).</span><span class="sxs-lookup"><span data-stu-id="fe25d-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="fe25d-109">Это можно сделать только для базовой установки уровня пользовательского интерфейса (/QB).</span><span class="sxs-lookup"><span data-stu-id="fe25d-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="fe25d-110">Кнопка **Отмена** скрыта для всей установки.</span><span class="sxs-lookup"><span data-stu-id="fe25d-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="fe25d-111">Дополнительные сведения см. в разделе [Параметры командной строки](command-line-options.md) и [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="fe25d-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="fe25d-112">Следующая командная строка скрывает кнопку **"Отмена"** и устанавливает Example.msi.</span><span class="sxs-lookup"><span data-stu-id="fe25d-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="fe25d-113">**msiexec/I example.msi/QB!**</span><span class="sxs-lookup"><span data-stu-id="fe25d-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="fe25d-114">Скрытие кнопки отмены в приложении или скрипте</span><span class="sxs-lookup"><span data-stu-id="fe25d-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="fe25d-115">Можно написать приложение или сценарий, чтобы скрыть кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="fe25d-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="fe25d-116">Это можно сделать только для базовой установки уровня пользовательского интерфейса, чтобы кнопка **отмены** была скрыта для всей установки.</span><span class="sxs-lookup"><span data-stu-id="fe25d-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="fe25d-117">Чтобы скрыть кнопку отмены в приложении, задайте ИНСТАЛЛУИЛЕВЕЛ \_ хидеканцел при вызове [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="fe25d-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="fe25d-118">В следующем примере скрывается кнопка **Отмена** и выполняется установка Example.msi.</span><span class="sxs-lookup"><span data-stu-id="fe25d-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



<span data-ttu-id="fe25d-119">Чтобы скрыть кнопку **Отмена** из скрипта, добавьте мсиуилевелхидеканцел в свойство [**duilevel**](installer-uilevel.md) [**объекта установщика**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="fe25d-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="fe25d-120">Следующий пример сценария VBScript скрывает кнопку **"Отмена"** и устанавливает Example.msi.</span><span class="sxs-lookup"><span data-stu-id="fe25d-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="fe25d-121">Скрытие кнопки отмены для частей установки с помощью настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="fe25d-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="fe25d-122">При установке можно скрыть и отобразить кнопку **Отмена** во время частей установки, отправив \_ сообщение инсталлмессаже коммондата с помощью пользовательского действия или сценариев библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="fe25d-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="fe25d-123">Дополнительные сведения см. в статьях [библиотеки динамической компоновки](dynamic-link-libraries.md), [сценарии](scripts.md), [пользовательские действия](custom-actions.md)и [Отправка сообщений в установщик Windows с помощью мсипроцессмессаже](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="fe25d-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="fe25d-124">Вызов настраиваемого действия должен предоставить запись.</span><span class="sxs-lookup"><span data-stu-id="fe25d-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="fe25d-125">Поле 1 этой записи должно содержать значение 2 (два), чтобы указать кнопку **отмены** .</span><span class="sxs-lookup"><span data-stu-id="fe25d-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="fe25d-126">Поле 2 должно содержать либо значение 0, либо 1.</span><span class="sxs-lookup"><span data-stu-id="fe25d-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="fe25d-127">Значение 0 в поле 2 скрывает кнопку, а значение 1 в поле 2 — скрытие кнопки.</span><span class="sxs-lookup"><span data-stu-id="fe25d-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="fe25d-128">Обратите внимание, что выделение записи размером 2 с [**мсикреатерекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) предоставляет поля 0, 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="fe25d-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="fe25d-129">Следующий пример настраиваемого действия библиотеки DLL скрывает кнопку **отмены** .</span><span class="sxs-lookup"><span data-stu-id="fe25d-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



<span data-ttu-id="fe25d-130">Следующее настраиваемое действие VBScript скрывает кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="fe25d-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



