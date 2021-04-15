---
description: Класс Кпоспасссру обрабатывает команды Seek для фильтров преобразования, передавая их в следующий фильтр.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Класс Кпоспасссру (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668575"
---
# <a name="cpospassthru-class"></a>Класс Кпоспасссру

![Иерархия базового класса кпоспасссру](images/cutil14.png)

`CPosPassThru`Класс обрабатывает команды Seek для фильтров преобразования, передавая их в следующий фильтр.

Когда приложение выполняет поиск графа фильтра, диспетчер графа фильтров передает команду Seek фильтрам модуля подготовки отчетов. Команда передается в качестве выходного ПИН-кода каждого фильтра, пока не достигнет фильтра, который может выполнить команду (если она есть). Дополнительные сведения см. в разделе [Поиск](seeking.md). `CPosPassThru`Класс передает все команды поиска в выходной закрепление вышестоящего фильтра, как показано на следующей схеме.

![класс кпоспасссру отправляет команды поиска в виде вышестоящего потока.](images/cpospassthru.png)

Хотя этот класс предоставляется в библиотеке базовых классов, DirectShow также предоставляет тот же класс в Quartz.dll. Использование Quartz.dll версии может немного уменьшить размер кода в фильтре, так как класс загружается во время выполнения из библиотеки DLL. Чтобы использовать эту версию, вызовите функцию [**креатепоспасссру**](createpospassthru.md) .

В методе **нонделегатингкуеринтерфаце** выходного контакта делегируйте объекту **кпоспасссру** каждый раз, когда запрошенный интерфейс является [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) или [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), как показано в следующем коде:


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



За исключением указанных случаев, все методы [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) и [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) в этом классе вызывают соответствующий метод для подключенного ПИН-кода и возвращают результат.



| Открытые методы                                                    | Описание                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**кпоспасссру**](cpospassthru-cpospassthru.md)                 | Метод конструктора.                                                                                 |
| [**форцерефреш**](cpospassthru-forcerefresh.md)                 | Является устаревшей.                                                                                           |
| [**жетмедиатиме**](cpospassthru-getmediatime.md)                 | Извлекает метки времени для текущего образца. Виртуализаци.                                           |
| Методы Имедиапоситион                                            | Описание                                                                                         |
| [**получить \_ Длительность**](cpospassthru-get-duration.md)                | Возвращает длительность потока.                                                               |
| [**разместить \_ CurrentPosition**](cpospassthru-put-currentposition.md)  | Задает текущую точку относительно общей продолжительности потока.                            |
| [**получить \_ StopTime**](cpospassthru-get-stoptime.md)                | Возвращает время, когда воспроизведение будет прервано относительно длительности потока.         |
| [**разместить \_ StopTime**](cpospassthru-put-stoptime.md)                | Задает время, когда воспроизведение будет прервано относительно длительности потока.              |
| [**получить \_ прероллтиме**](cpospassthru-get-prerolltime.md)          | Извлекает объем данных, которые будут помещены в очередь перед начальной позицией.                         |
| [**разместить \_ прероллтиме**](cpospassthru-put-prerolltime.md)          | Задает объем данных, которые будут помещены в очередь перед начальной позицией.                              |
| [**получить \_ скорость**](cpospassthru-get-rate.md)                        | Возвращает скорость воспроизведения.                                                                        |
| [**\_скорость размещения**](cpospassthru-put-rate.md)                        | Задает скорость воспроизведения.                                                                             |
| [**получить \_ CurrentPosition**](cpospassthru-get-currentposition.md)  | Извлекает текущую координату относительно общей продолжительности потока.                       |
| [**кансикфорвард**](cpospassthru-canseekforward.md)             | Определяет, можно ли выполнить поиск в потоке назад.                                               |
| [**кансикбакквард**](cpospassthru-canseekbackward.md)           | Определяет, можно ли выполнить поиск в потоке вперед.                                                |
| Методы Имедиасикинг                                             | Описание                                                                                         |
| [**чекккапабилитиес**](cpospassthru-checkcapabilities.md)       | Запрашивает, имеет ли поток указанные возможности поиска.                                        |
| [**конверттимеформат**](cpospassthru-converttimeformat.md)       | Преобразует из одного формата времени в другой.                                                           |
| [**Доступность**](cpospassthru-getavailable.md)                 | Извлекает диапазон времени, в течение которого поиск является эффективным.                                         |
| [**Возможности**](cpospassthru-getcapabilities.md)           | Извлекает все возможности поиска в потоке.                                               |
| [**жеткуррентпоситион**](cpospassthru-getcurrentposition.md)     | Извлекает текущую координату относительно общей продолжительности потока.                       |
| [**Длительное время**](cpospassthru-getduration.md)                   | Возвращает длительность потока.                                                               |
| [**Выстановки**](cpospassthru-getpositions.md)                 | Извлекает текущую и заданную позиции относительно общей продолжительности потока. |
| [**жетпреролл**](cpospassthru-getpreroll.md)                     | Извлекает объем данных, которые будут помещены в очередь перед начальной позицией.                         |
| [**Коэффициент**](cpospassthru-getrate.md)                           | Возвращает скорость воспроизведения.                                                                        |
| [**жетстоппоситион**](cpospassthru-getstopposition.md)           | Возвращает время, когда воспроизведение будет прервано относительно длительности потока.         |
| [**жеттимеформат**](cpospassthru-gettimeformat.md)               | Извлекает текущий формат времени.                                                                  |
| [**исформатсуппортед**](cpospassthru-isformatsupported.md)       | Определяет, поддерживается ли указанный формат времени.                                            |
| [**исусингтимеформат**](cpospassthru-isusingtimeformat.md)       | Определяет, является ли указанный формат времени используемым в данный момент форматом.                          |
| [**куерипреферредформат**](cpospassthru-querypreferredformat.md) | Возвращает предпочтительный формат времени для потока.                                                 |
| [**сетпоситионс**](cpospassthru-setpositions.md)                 | Установка текущей позиции и позиции окончания.                                                    |
| [**сетрате**](cpospassthru-setrate.md)                           | Задает скорость воспроизведения.                                                                             |
| [**сеттимеформат**](cpospassthru-settimeformat.md)               | Задает формат времени.                                                                               |
| Вспомогательные функции                                                  | Описание                                                                                         |
| [**креатепоспасссру**](createpospassthru.md)                    | Создает `CPosPassThru` объект или [**крендерерпоспасссру**](crendererpospassthru.md) .            |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




