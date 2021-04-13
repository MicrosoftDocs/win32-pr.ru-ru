---
title: Определение того, установлена ли роль службы удаленных рабочих столов
description: В. пример кода, в котором показан метод, возвращающий значение true, если роль сервера службы удаленных рабочих столов установлена и запущена, или значение false в противном случае, начиная с Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f7d094f88271346c97f8d0467b48a266c865d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413434"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Определение того, установлена ли роль службы удаленных рабочих столов

Чтобы определить, установлена ли роль сервера службы удаленных рабочих столов, можно использовать класс WMI [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) .

В следующем примере C# показан метод, возвращающий **значение true** , если роль сервера службы удаленных рабочих столов установлена и запущена, или **значение false** в противном случае. Так как класс WMI [**\_ ServerFeature для Win32**](/windows/desktop/WmiSdk/win32-serverfeature) доступен только начиная с Windows Server 2008, этот код не совместим с более ранними версиями Windows.


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 