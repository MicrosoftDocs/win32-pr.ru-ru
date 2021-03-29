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
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="59c03-104">Запрос состояния дополнительных функций</span><span class="sxs-lookup"><span data-stu-id="59c03-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="59c03-105">В Windows 7 WMI реализовала класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="59c03-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="59c03-106">Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.</span><span class="sxs-lookup"><span data-stu-id="59c03-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="59c03-107">Для запроса состояния дополнительных функций можно использовать командлеты Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="59c03-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="59c03-108">Во всех примерах в этом разделе используется командлет Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="59c03-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="59c03-109">Дополнительные сведения см. в разделе [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="59c03-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="59c03-110">**Получение всех экземпляров дополнительных компонентов, имеющихся на компьютере**</span><span class="sxs-lookup"><span data-stu-id="59c03-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="59c03-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="59c03-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="59c03-112">**Запрос дополнительных компонентов путем указания имени функции**</span><span class="sxs-lookup"><span data-stu-id="59c03-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="59c03-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="59c03-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="59c03-114">В свойстве **Name** учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="59c03-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="59c03-115">**Запрос дополнительных компонентов путем указания состояния установки**</span><span class="sxs-lookup"><span data-stu-id="59c03-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="59c03-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="59c03-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="59c03-117">Дополнительные сведения о возможных значениях свойства **InstallState** см. в разделе [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span><span class="sxs-lookup"><span data-stu-id="59c03-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59c03-118">См. также</span><span class="sxs-lookup"><span data-stu-id="59c03-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59c03-119">**\_Оптионалфеатуре Win32**</span><span class="sxs-lookup"><span data-stu-id="59c03-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
