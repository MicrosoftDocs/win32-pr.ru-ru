---
description: В Windows 7 WMI реализовала класс Win32 \_ оптионалфеатуре. Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Запрос состояния дополнительных функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812652"
---
# <a name="querying-the-status-of-optional-features"></a>Запрос состояния дополнительных функций

В Windows 7 WMI реализовала класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.

Для запроса состояния дополнительных функций можно использовать командлеты Windows PowerShell. Во всех примерах в этом разделе используется командлет Get-WmiObject. Дополнительные сведения см. в разделе [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Получение всех экземпляров дополнительных компонентов, имеющихся на компьютере**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**Запрос дополнительных компонентов путем указания имени функции**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > В свойстве **Name** учитывается регистр.

     

**Запрос дополнительных компонентов путем указания состояния установки**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    Дополнительные сведения о возможных значениях свойства **InstallState** см. в разделе [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**\_Оптионалфеатуре Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
