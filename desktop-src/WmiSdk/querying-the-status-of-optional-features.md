---
description: в Windows 7 инструментарий WMI реализовал \_ класс Win32 оптионалфеатуре. Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Запрос состояния дополнительных функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996034"
---
# <a name="querying-the-status-of-optional-features"></a>Запрос состояния дополнительных функций

в Windows 7 инструментарий WMI реализовал класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.

для запроса состояния дополнительных функций можно использовать командлеты Windows PowerShell. Во всех примерах в этом разделе используется командлет Get-WmiObject. Дополнительные сведения см. в разделе [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**\_Оптионалфеатуре Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
