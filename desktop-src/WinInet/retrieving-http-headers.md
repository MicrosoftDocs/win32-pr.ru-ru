---
title: Получение заголовков HTTP
description: В этом учебнике описывается получение сведений о заголовках из HTTP-запросов.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955514"
---
# <a name="retrieving-http-headers"></a>Получение заголовков HTTP

В этом учебнике описывается получение сведений о заголовках из HTTP-запросов.

## <a name="implementation-steps"></a>Шаги реализации

Получить сведения о заголовке можно двумя способами:

-   Используйте одну из констант [**флагов сведений о запросе**](query-info-flags.md) , связанных с заголовком HTTP, которое требуется вашему приложению.
-   Используйте \_ \_ флаг настраиваемого атрибута http-запроса и передайте имя HTTP-заголовка.

Использование константы, связанной с заголовком HTTP, которую требуется вашему приложению, выполняется быстрее, но могут существовать заголовки HTTP, с которыми не связана константа. В таких случаях доступен метод, использующий \_ \_ флаг настраиваемого атрибута http-запроса.

Оба метода используют функцию [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**Хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) принимает маркер [**хинтернет**](appendix-a-hinternet-handles.md) , на котором был сделан HTTP-запрос, один атрибут, буфер, значение DWORD, содержащее размер буфера, и значение индекса. Модификатор можно также добавить к атрибуту, переданному в [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) , чтобы указать, в каком формате должны возвращаться данные.

### <a name="retrieving-headers-using-a-constant"></a>Получение заголовков с помощью константы

Чтобы использовать функцию [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) для получения заголовка HTTP с помощью константы, выполните следующие действия.

1.  Вызовите [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с константой из списка [**Attributes**](query-info-flags.md) , **пустым** буфером и переменной, содержащей размер буфера, равным нулю. Кроме того, если приложению требуются данные в определенном формате, можно добавить константу из списка [**модификаторов**](query-info-flags.md) .
2.  Если запрошенный заголовок HTTP существует, вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) должен завершиться ошибкой, аргумент [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) должен возвращать ошибку, \_ недостаточную \_ для буфера, а переменная, передаваемая для параметра *лпдвбуфферленгс* , должна быть установлена в соответствии с требуемым числом байтов.
3.  Выделение буфера с требуемым числом байтов.
4.  Повторите вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

В следующем примере демонстрируется вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с помощью \_ \_ необработанных \_ заголовков HTTP-запроса \_ , который представляет собой специальное значение, запрашивающее все возвращенные заголовки HTTP.


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a>Получение заголовков с помощью пользовательского HTTP- \_ запроса \_

Чтобы использовать функцию [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) для получения заголовка HTTP с помощью HTTP- \_ запроса \_ Custom, выполните следующие действия.

1.  Выделите буфер, достаточно большой для хранения строкового имени заголовка HTTP.
2.  Запишите строковое имя заголовка HTTP в буфер.
3.  Вызовите [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с HTTP- \_ запросом \_ Custom, буфер, содержащий строковое имя заголовка HTTP, и переменную, которая содержит размер буфера. Кроме того, если приложению требуются данные в определенном формате, можно добавить константу из списка [**модификаторов**](query-info-flags.md) .
4.  Если вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) завершается ошибкой и [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ недостаточно \_ буфера, перераспределите буфер с требуемым числом байтов.
5.  Снова введите строковое имя заголовка HTTP в буфер.
6.  Повторите вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

В следующем примере демонстрируется вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с использованием \_ \_ пользовательской константы HTTP-запроса для запроса заголовка HTTP Content-Type.


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 