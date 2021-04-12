---
title: Перечисление сетевых ресурсов
description: В следующем примере показана определяемая приложением функция (Енумератефунк), которая перечисляет все ресурсы в сети.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313e679746b09603d2514b418abf281fefa9bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413304"
---
# <a name="enumerating-network-resources"></a>Перечисление сетевых ресурсов

В следующем примере показана определяемая приложением функция (Енумератефунк), которая перечисляет все ресурсы в сети. В примере указывается **значение NULL** для указателя на структуру [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , так как когда [**внетопененум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) получает **пустой** указатель, он получает маркер в корне сети.

Чтобы начать перечисление ресурса сетевого контейнера, приложение должно выполнить следующие действия.

1.  Передайте адрес структуры [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , которая представляет ресурс, в функцию [**внетопененум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .
2.  Выделите буфер, достаточно большой для хранения массива структур [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , возвращаемых функцией [**внетенумресаурце**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) , а также строки, в которые они указывают элементы.
3.  Передайте в функцию [**внетенумресаурце**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) маркер ресурса, возвращенный функцией [**внетопененум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .
4.  Закройте обработчик ресурсов, если он больше не нужен, вызвав функцию [**внетклосинум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) .

Можно продолжить перечисление ресурса контейнера, описанного в массиве структур [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , полученных [**внетенумресаурце**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea). Если элемент **двусаже** структуры **нетресаурце** равен RESOURCEUSAGE \_ Container, передайте адрес структуры в функцию [**внетопененум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) , чтобы открыть контейнер и продолжить перечисление. Если **двусаже** равно RESOURCEUSAGE \_ Connected, приложение может передать адрес структуры в функцию [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) или функцию [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) для подключения к ресурсу.

Сначала в примере вызывается функция [**внетопененум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) , чтобы начать перечисление. В примере вызывается функция [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) для выделения требуемого буфера, а затем вызывается функция [**зеромемори**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) , чтобы установить содержимое буфера в ноль. Затем в примере вызывается функция [**внетенумресаурце**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) , чтобы продолжить перечисление. Каждый раз, когда элемент **двусаже** структуры [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) , извлеченной **внетенумресаурце** , равен RESOURCEUSAGE \_ Container, функция енумератефунк вызывает саму себя рекурсивно и использует указатель на эту структуру в своем вызове к **внетопененум**. Наконец, в примере вызывается функция [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) для высвобождения выделенной памяти и [**внетклосинум**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) для завершения перечисления.


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



Дополнительные сведения об использовании определяемого приложением обработчика ошибок см. в разделе [получение сетевых ошибок](retrieving-network-errors.md).

 

 