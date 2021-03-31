---
description: Существует несколько типов запросов, которые предназначены для запроса состояния ресурсов.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Запросы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894085"
---
# <a name="queries-direct3d-9"></a>Запросы (Direct3D 9)

Существует несколько типов запросов, которые предназначены для запроса состояния ресурсов. Состояние данного ресурса включает состояние графического процессора (GPU), состояние драйвера или состояние среды выполнения. Чтобы понять разницу между различными типами запросов, необходимо понимать состояния запросов. На следующей схеме перехода состояния объясняются все состояния запросов.

![Диаграмма, показывающая переходы между состояниями запросов](images/queries.png)

На схеме показаны три состояния, каждое из которых определяется круговыми кругами. Каждая из сплошных линий — это события, управляемые приложениями, которые вызывают переход между состояниями. Пунктирная линия является событием, управляемым на основе ресурсов, которое переключает запрос из выданного состояния в сигнальное состояние. Каждое из этих состояний имеет другую цель:

-   Сигнальное состояние похоже на состояние простоя. Объект запроса создан и ожидает, пока приложение выдаст запрос. После завершения запроса и передачи обратно в сигнальное состояние можно получить ответ на запрос.
-   Состояние здания похоже на промежуточную область для запроса. Из состояния здания был выдан запрос (с помощью вызова [**D3DISSUE \_ Begin**](d3dissue-begin.md)), но еще не перешел в состояние выданного. Когда приложение выдает окончание запроса (путем вызова [**D3DISSUE \_ End**](d3dissue-end.md)), запрос переходит в состояние «выдано».
-   Выданное состояние означает, что запрашиваемый ресурс имеет контроль над запросом. Когда ресурс завершит свою работу, ресурс переводит конечный автомат в сигнальное состояние. Во время выданного состояния приложение должно выполнить опрос, чтобы обнаружить переход в сигнальное состояние. После перехода в сигнальное состояние метод [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) возвращает приложению результат запроса (через аргумент).

В следующей таблице перечислены доступные типы запросов.



| Тип запроса        | Событие проблемы                                                                      | Буфер GetData                                                              | Параметры выполнения      | Неявное начало запроса                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| бандвидстимингс  | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Розничная или отладочная | Н/Д                                              |
| качеутилизатион  | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Розничная или отладочная | Н/Д                                              |
| ЖУРНАЛЕ             | [**D3DISSUE \_ конец**](d3dissue-end.md)                                            | BOOL                                                                        | Розничная или отладочная | [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| интерфацетимингс  | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Розничная или отладочная | Н/Д                                              |
| ПЕРЕКРЫТИЯ         | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | DWORD                                                                       | Розничная или отладочная | Н/Д                                              |
| пипелинетимингс   | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Розничная или отладочная | Н/Д                                              |
| RESOURCEMANAGER   | [**D3DISSUE \_ конец**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Только Отладка   | [**Настоящее**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ конец**](d3dissue-end.md)                                            | UINT64                                                                      | Розничная или отладочная | Н/Д                                              |
| тиместампдисжоинт | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | BOOL                                                                        | Розничная или отладочная | Н/Д                                              |
| тиместампфрек     | [**D3DISSUE \_ конец**](d3dissue-end.md)                                            | UINT64                                                                      | Розничная или отладочная | Н/Д                                              |
| вкаче            | [**D3DISSUE \_ конец**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ вкаче**](d3ddevinfo-vcache.md)                             | Розничная или отладочная | [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| вертексстатс       | [**D3DISSUE \_ конец**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Только Отладка   | [**Настоящее**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| вертекстимингс     | [**D3DISSUE \_ Начало**](d3dissue-begin.md), [ **D3DISSUE \_**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Розничная или отладочная | Н/Д                                              |



 

Для некоторых запросов требуется событие Begin и End, а для других требуется только завершающее событие. Запросы, для которых требуется событие End, начинаются только при возникновении другого неявного события (которое перечислено в таблице). Все запросы возвращают ответ, за исключением запроса события, ответ которого всегда равен **true**. Приложение использует либо состояние запроса, либо код возврата [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Создание запроса

Перед созданием запроса можно проверить, поддерживает ли среда выполнения запросы, вызвав [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) со **следующим указателем** :


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Этот метод возвращает код успешного выполнения, если может быть создан запрос. в противном случае возвращается код ошибки. После выполнения [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) можно создать объект запроса следующим образом:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Если этот вызов будет выполнен, создается объект запроса. Запрос в основном бездействует в сигнальном состоянии (с неинициализированным ответом), ожидающим выполнения. Завершив работу с запросом, отпустите его как любой другой интерфейс.

## <a name="issue-a-query"></a>Выдача запроса

Приложение изменяет состояние запроса, выдавая запрос. Ниже приведен пример выдачи запроса.


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Запрос в сигнальном состоянии будет перенесен следующим образом:



| Тип проблемы                                | Запрос переходит к. . . |
|-------------------------------------------|--------------------------------|
| [**\_Начало D3DISSUE**](d3dissue-begin.md) | Состояние сборки.                |
| [**D3DISSUE \_ конец**](d3dissue-end.md)     | Состояние выдано.                  |



 

Запрос в состоянии здания будет перенесен следующим образом:



| Тип проблемы                                | Запрос переходит к. . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**\_Начало D3DISSUE**](d3dissue-begin.md) | (Нет перехода, остается в состоянии здания. Перезапускает скобку запроса.) |
| [**D3DISSUE \_ конец**](d3dissue-end.md)     | Состояние выдано.                                                             |



 

Запрос в выданном состоянии будет перенесен следующим образом:



| Тип проблемы                                | Запрос переходит к. . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**\_Начало D3DISSUE**](d3dissue-begin.md) | Состояние сборки и перезапускает скобку запроса.    |
| [**D3DISSUE \_ конец**](d3dissue-end.md)     | Выданное состояние после прерывания существующего запроса. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Проверка состояния запроса и получение ответа на запрос

Метод [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) выполняет два действия:

1.  Возвращает состояние запроса в коде возврата.
2.  Возвращает ответ на запрос в *pData*.

В каждом из трех состояний запроса приведены коды возврата [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :



| Состояние запроса | Код возврата GetData |
|-------------|---------------------|
| Сигнал    | \_ОК               |
| Сборка    | Код ошибки          |
| Выдано      | S \_ false            |



 

Например, если запрос находится в состоянии «выдано» и ответ на запрос недоступен, функция [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) возвращает \_ значение false. Когда ресурс завершает свою работу и приложение выпустило завершение запроса, ресурс переводит запрос в сигнальное состояние. Из состояния "сигнал" функция **GetData** возвращает S \_ ОК, что означает, что ответ на запрос также возвращается в *pData*. Например, ниже приведена последовательность событий для возврата количества пикселей, рисуемых в последовательности отрисовки.

-   создание запроса;
-   Выдача события Begin.
-   Нарисуйте что-нибудь.
-   Выдача завершающего события.

Ниже приведена соответствующая последовательность кода.


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



Эти строки кода выполняют несколько задач:

-   Вызовите [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) , чтобы получить количество рисуемых пикселей.
-   Укажите [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) , чтобы разрешить ресурсу переводить запрос в сигнальное состояние.
-   Опросить ресурс запроса, вызвав метод [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) из цикла. Пока метод **GetData** возвращает \_ значение false, это означает, что ресурс еще не вернул ответ.

Возвращаемое значение [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) , по сути, указывает, в каком состоянии находится запрос. Возможные значения: S \_ OK, s \_ false и ошибка. Не вызывайте **GetData** для запроса, который находится в состоянии здания.

-   \_ОК означает, что ресурс (GPU или драйвер или среда выполнения) завершен. Запрос возвращается в сигнальное состояние. Ответ (если таковой имеется) возвращается методом [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).
-   \_Значение false означает, что ресурс (GPU или драйвер или среда выполнения) еще не может вернуть ответ. Это может быть вызвано тем, что графический процессор не завершен или пока не просмотрел работу.
-   Ошибка означает, что запрос создал ошибку, которую невозможно восстановить. Это может быть так, если устройство потеряно во время выполнения запроса. После создания запроса об ошибке (отличном от S \_ false) запрос должен быть создан повторно, что приведет к перезапуску последовательности запросов из сигнального состояния.

Вместо указания [**D3DGETDATA \_ flush**](d3dgetdata-flush.md), которая предоставляет более актуальную информацию, можно указать ноль, которая является более неплотной, если запрос находится в состоянии «выдано». Если указать нуль, то [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) не будет сбрасывать буфер команд. По этой причине необходимо соблюдать осторожность, чтобы избежать циклов инфинате (Дополнительные сведения см. в разделе **GetData** ). Так как среда выполнения помещает в очередь работу в буфере команд, **D3DGETDATA \_ flush** — это механизм сброса буфера команд в драйвер (и, следовательно, графический процессор; см. раздел [Точная профилирование вызовов API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Во время очистки буфера команд запрос может перейти в сигнальное состояние.

## <a name="example-an-event-query"></a>Пример. запрос события

Запрос события не поддерживает событие Begin.

-   создание запроса;
-   Выдача завершающего события.
-   Опросить, пока GPU не простаивает.
-   Выдача завершающего события.


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



Это последовательность команд, которые запрос на событие использует для профилирования вызовов интерфейса прикладного программирования (API) (см. раздел [Точная профилирование вызовов API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). В этой последовательности используются маркеры, помогающие управлять объемом работы в буфере команд.

Обратите внимание, что приложения должны уделять особое внимание значительным затратам на очистку буфера команд, так как в этом случае операционная система переключается в режим ядра, что приводит к снижению производительности немалым. Приложения также должны знать о расходе циклов ЦП, ожидая завершения запросов.

Запросы — это оптимизация, которую следует использовать во время отрисовки для повышения производительности. Поэтому не стоит тратить время на ожидание завершения запроса. Если выдается запрос и результаты еще не готовы к моменту их проверки приложением, то попытки оптимизации не выполнялись успешно, а отрисовка должна продолжаться как обычно.

Классический пример — во время отбора перекрытия. Вместо приведенного выше цикла **while** приложение, использующее запросы, может реализовать перекрытияное извлечение, чтобы проверить, завершился ли запрос на время, необходимое для результата. Если запрос не завершен, продолжайте (как наихудший сценарий), как если проверяемый объект не перекрыто (т. е. он является видимым) и готовит его к просмотру. Код будет выглядеть примерно так:


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Дополнительные разделы](advanced-topics.md)
</dt> </dl>

 

 
