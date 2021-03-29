---
title: Перечисление контроллеров домена
description: В более ранних версиях Windows приложение могло получить только один контроллер домена в домене, вызвав DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, перечисление контроллеров домена Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773232"
---
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="b3511-104">Перечисление контроллеров домена</span><span class="sxs-lookup"><span data-stu-id="b3511-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="b3511-105">В более ранних версиях Windows приложение могло получить только один контроллер домена в домене, вызвав [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span><span class="sxs-lookup"><span data-stu-id="b3511-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="b3511-106">Не существовало способа предсказать, какой контроллер домена будет извлечен, или получить список контроллеров домена.</span><span class="sxs-lookup"><span data-stu-id="b3511-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="b3511-107">Windows позволяет приложению перечислять контроллеры домена в домене с помощью функций [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)и [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="b3511-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="b3511-108">Чтобы перечислить контроллер домена, вызовите [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span><span class="sxs-lookup"><span data-stu-id="b3511-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="b3511-109">Эта функция принимает параметры, определяющие домен для перечисления и другие параметры перечисления.</span><span class="sxs-lookup"><span data-stu-id="b3511-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="b3511-110">**Дсжетдкопен** предоставляет обработчик контекста перечисления доменов, который используется для обнаружения операции перечисления при вызове [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) и [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="b3511-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="b3511-111">Функция [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) вызывается с помощью обработчика контекста перечисления доменов для получения следующего контроллера домена в перечислении.</span><span class="sxs-lookup"><span data-stu-id="b3511-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="b3511-112">При первом вызове этой функции первый контроллер домена в перечислении извлекается.</span><span class="sxs-lookup"><span data-stu-id="b3511-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="b3511-113">При втором вызове этой функции извлекается второй контроллер домена в перечислении.</span><span class="sxs-lookup"><span data-stu-id="b3511-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="b3511-114">Этот процесс повторяется до тех пор, пока **дсжетдкнекст** **не вернет ошибку больше \_ \_ \_ элементов**, что указывает на конец перечисления.</span><span class="sxs-lookup"><span data-stu-id="b3511-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="b3511-115">Функция [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) будет перечислять контроллеры домена в двух группах.</span><span class="sxs-lookup"><span data-stu-id="b3511-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="b3511-116">Первая группа содержит контроллеры домена, охватывающие сайт компьютера, на котором выполняется функция, а вторая группа содержит контроллеры домена, не охватывающие сайт компьютера, на котором выполняется функция.</span><span class="sxs-lookup"><span data-stu-id="b3511-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="b3511-117">Если в параметре *оптионфлагс* в [**Дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)указан флаг **службы каталогов \_ Notify \_ после \_ \_ записи сайта** , функция **дсжетдкнекст** вернет **ошибку \_ метка файла, \_ обнаруженную** после получения всех контроллеров домена для конкретного сайта.</span><span class="sxs-lookup"><span data-stu-id="b3511-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="b3511-118">Затем **дсжетдкнекст** начнет перечислить вторую группу, которая содержит все контроллеры домена в домене, включая контроллеры домена для конкретного сайта, содержащиеся в первой группе.</span><span class="sxs-lookup"><span data-stu-id="b3511-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="b3511-119">Сначала перечисляются контроллеры домена, обрабатывающие сайт компьютера, на котором выполняется функция, за которыми следуют контроллеры домена, не охватывающие сайт компьютера, на котором выполняется функция.</span><span class="sxs-lookup"><span data-stu-id="b3511-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="b3511-120">Считается, что контроллер домена охватывает сайт, если контроллер домена настроен для размещения на этом сайте, или если контроллер домена находится на сайте, который находится ближе всего к рассматриваемому узлу, с точки зрения настроенной стоимости межсайтовых связей.</span><span class="sxs-lookup"><span data-stu-id="b3511-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="b3511-121">При наличии контроллеров домена в группе контроллеров домена, которые охватывают и группы контроллеров домена, не охватывающих сайт компьютера, контроллеры домена возвращаются в группе в порядке их настроенных приоритетов и весов, указанных в DNS.</span><span class="sxs-lookup"><span data-stu-id="b3511-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="b3511-122">Контроллеры домена с меньшим числовым приоритетом возвращаются в группе первыми.</span><span class="sxs-lookup"><span data-stu-id="b3511-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="b3511-123">Если в группе, связанной с сайтами, имеется подгруппа нескольких контроллеров домена с одинаковым приоритетом, то контроллеры домена возвращаются в взвешенном случайном порядке, где контроллеры домена с более высоким весом имеют больше вероятностей, которые будут возвращены первыми.</span><span class="sxs-lookup"><span data-stu-id="b3511-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="b3511-124">Сайты, приоритеты и веса настраиваются администратором домена для достижения эффективной производительности и балансировки нагрузки между несколькими контроллерами домена, доступными в домене.</span><span class="sxs-lookup"><span data-stu-id="b3511-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="b3511-125">По этой причине приложения, использующие функции [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) , автоматически используют преимущества этих оптимизаций.</span><span class="sxs-lookup"><span data-stu-id="b3511-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="b3511-126">Если перечисление завершено или больше не требуется, перечисление должно быть закрыто путем вызова [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) с помощью обработчика контекста перечисления доменов.</span><span class="sxs-lookup"><span data-stu-id="b3511-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="b3511-127">Чтобы сбросить перечисление, необходимо закрыть текущее перечисление, вызвав [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) , а затем снова открыть перечисление, вызвав [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) еще раз.</span><span class="sxs-lookup"><span data-stu-id="b3511-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="b3511-128">Пример</span><span class="sxs-lookup"><span data-stu-id="b3511-128">Example</span></span>

<span data-ttu-id="b3511-129">В следующем примере кода показано, как использовать эти функции для перечисления контроллеров домена в локальном домене.</span><span class="sxs-lookup"><span data-stu-id="b3511-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




