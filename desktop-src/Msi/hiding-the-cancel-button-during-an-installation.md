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
# <a name="hiding-the-cancel-button-during-an-installation"></a>Скрытие кнопки "Отмена" во время установки

Можно скрыть кнопку **Отмена** , которая используется для отмены установки, с помощью параметра командной строки, установщик Windows API или настраиваемого действия. Кнопка **Отмена** может быть скрыта для части или всей установки в зависимости от используемого метода.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Скрытие кнопки "Отмена" из командной строки

Во время установки кнопка **Отмена** может быть скрыта с помощью параметра командной строки (!). Это можно сделать только для базовой установки уровня пользовательского интерфейса (/QB). Кнопка **Отмена** скрыта для всей установки. Дополнительные сведения см. в разделе [Параметры командной строки](command-line-options.md) и [уровни пользовательского интерфейса](user-interface-levels.md). Следующая командная строка скрывает кнопку **"Отмена"** и устанавливает Example.msi.

**msiexec/I example.msi/QB!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Скрытие кнопки отмены в приложении или скрипте

Можно написать приложение или сценарий, чтобы скрыть кнопку **Отмена** . Это можно сделать только для базовой установки уровня пользовательского интерфейса, чтобы кнопка **отмены** была скрыта для всей установки.

Чтобы скрыть кнопку отмены в приложении, задайте ИНСТАЛЛУИЛЕВЕЛ \_ хидеканцел при вызове [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). В следующем примере скрывается кнопка **Отмена** и выполняется установка Example.msi.


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



Чтобы скрыть кнопку **Отмена** из скрипта, добавьте мсиуилевелхидеканцел в свойство [**duilevel**](installer-uilevel.md) [**объекта установщика**](installer-object.md). Следующий пример сценария VBScript скрывает кнопку **"Отмена"** и устанавливает Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Скрытие кнопки отмены для частей установки с помощью настраиваемого действия

При установке можно скрыть и отобразить кнопку **Отмена** во время частей установки, отправив \_ сообщение инсталлмессаже коммондата с помощью пользовательского действия или сценариев библиотеки DLL. Дополнительные сведения см. в статьях [библиотеки динамической компоновки](dynamic-link-libraries.md), [сценарии](scripts.md), [пользовательские действия](custom-actions.md)и [Отправка сообщений в установщик Windows с помощью мсипроцессмессаже](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Вызов настраиваемого действия должен предоставить запись. Поле 1 этой записи должно содержать значение 2 (два), чтобы указать кнопку **отмены** . Поле 2 должно содержать либо значение 0, либо 1. Значение 0 в поле 2 скрывает кнопку, а значение 1 в поле 2 — скрытие кнопки. Обратите внимание, что выделение записи размером 2 с [**мсикреатерекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) предоставляет поля 0, 1 и 2.

Следующий пример настраиваемого действия библиотеки DLL скрывает кнопку **отмены** .


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



Следующее настраиваемое действие VBScript скрывает кнопку **Отмена** .


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



 

 



