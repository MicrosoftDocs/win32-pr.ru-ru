---
title: Определение того, установлена ли роль службы удаленных рабочих столов
description: в. пример кода, в котором показан метод, возвращающий значение True, если роль сервера службы удаленных рабочих столов установлена и запущена, или значение false в противном случае, начиная с Windows server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf7ac1932c32ea797783d04f4e279bab03339c9b7620c11e72d4b755f084736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871764"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Определение того, установлена ли роль службы удаленных рабочих столов

Чтобы определить, установлена ли роль сервера службы удаленных рабочих столов, можно использовать класс WMI [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) .

В следующем примере C# показан метод, возвращающий **значение true** , если роль сервера службы удаленных рабочих столов установлена и запущена, или **значение false** в противном случае. так как класс WMI [**\_ ServerFeature для Win32**](/windows/desktop/WmiSdk/win32-serverfeature) доступен только начиная с Windows Server 2008, этот код не совместим с более ранними версиями Windows.


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



 

 