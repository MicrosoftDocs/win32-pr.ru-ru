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
# <a name="enumerating-domain-controllers"></a>Перечисление контроллеров домена

В более ранних версиях Windows приложение могло получить только один контроллер домена в домене, вызвав [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). Не существовало способа предсказать, какой контроллер домена будет извлечен, или получить список контроллеров домена. Windows позволяет приложению перечислять контроллеры домена в домене с помощью функций [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)и [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Чтобы перечислить контроллер домена, вызовите [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena). Эта функция принимает параметры, определяющие домен для перечисления и другие параметры перечисления. **Дсжетдкопен** предоставляет обработчик контекста перечисления доменов, который используется для обнаружения операции перечисления при вызове [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) и [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Функция [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) вызывается с помощью обработчика контекста перечисления доменов для получения следующего контроллера домена в перечислении. При первом вызове этой функции первый контроллер домена в перечислении извлекается. При втором вызове этой функции извлекается второй контроллер домена в перечислении. Этот процесс повторяется до тех пор, пока **дсжетдкнекст** **не вернет ошибку больше \_ \_ \_ элементов**, что указывает на конец перечисления.

Функция [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) будет перечислять контроллеры домена в двух группах. Первая группа содержит контроллеры домена, охватывающие сайт компьютера, на котором выполняется функция, а вторая группа содержит контроллеры домена, не охватывающие сайт компьютера, на котором выполняется функция. Если в параметре *оптионфлагс* в [**Дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)указан флаг **службы каталогов \_ Notify \_ после \_ \_ записи сайта** , функция **дсжетдкнекст** вернет **ошибку \_ метка файла, \_ обнаруженную** после получения всех контроллеров домена для конкретного сайта. Затем **дсжетдкнекст** начнет перечислить вторую группу, которая содержит все контроллеры домена в домене, включая контроллеры домена для конкретного сайта, содержащиеся в первой группе.

Сначала перечисляются контроллеры домена, обрабатывающие сайт компьютера, на котором выполняется функция, за которыми следуют контроллеры домена, не охватывающие сайт компьютера, на котором выполняется функция. Считается, что контроллер домена охватывает сайт, если контроллер домена настроен для размещения на этом сайте, или если контроллер домена находится на сайте, который находится ближе всего к рассматриваемому узлу, с точки зрения настроенной стоимости межсайтовых связей. При наличии контроллеров домена в группе контроллеров домена, которые охватывают и группы контроллеров домена, не охватывающих сайт компьютера, контроллеры домена возвращаются в группе в порядке их настроенных приоритетов и весов, указанных в DNS. Контроллеры домена с меньшим числовым приоритетом возвращаются в группе первыми. Если в группе, связанной с сайтами, имеется подгруппа нескольких контроллеров домена с одинаковым приоритетом, то контроллеры домена возвращаются в взвешенном случайном порядке, где контроллеры домена с более высоким весом имеют больше вероятностей, которые будут возвращены первыми. Сайты, приоритеты и веса настраиваются администратором домена для достижения эффективной производительности и балансировки нагрузки между несколькими контроллерами домена, доступными в домене. По этой причине приложения, использующие функции [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) , автоматически используют преимущества этих оптимизаций.

Если перечисление завершено или больше не требуется, перечисление должно быть закрыто путем вызова [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) с помощью обработчика контекста перечисления доменов.

Чтобы сбросить перечисление, необходимо закрыть текущее перечисление, вызвав [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) , а затем снова открыть перечисление, вызвав [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) еще раз.

## <a name="example"></a>Пример

В следующем примере кода показано, как использовать эти функции для перечисления контроллеров домена в локальном домене.


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



 

 




