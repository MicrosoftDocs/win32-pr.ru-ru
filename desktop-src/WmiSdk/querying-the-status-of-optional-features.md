---
description: в Windows 7 инструментарий WMI реализовал \_ класс Win32 оптионалфеатуре. Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Запрос состояния дополнительных функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecffe6ddbe9b860c6f49fe12d3fed500c169bef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476710"
---
# <a name="querying-the-status-of-optional-features"></a>Запрос состояния дополнительных функций

в Windows 7 инструментарий WMI реализовал класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.

для запроса состояния дополнительных функций можно использовать командлеты Windows PowerShell. Во всех примерах в этом разделе используется командлет Get-WmiObject. Дополнительные сведения см. в разделе [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Получение всех экземпляров дополнительных компонентов, имеющихся на компьютере**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**Запрос дополнительных компонентов путем указания имени функции**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**Запрос дополнительных компонентов путем указания состояния установки**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**\_Оптионалфеатуре Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
