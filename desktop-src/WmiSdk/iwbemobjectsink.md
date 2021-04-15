---
description: Интерфейс Ивбемобжектсинк создает интерфейс приемника, который может получать все типы уведомлений в модели программирования WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Интерфейс Ивбемобжектсинк (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683217"
---
# <a name="iwbemobjectsink-interface"></a>Интерфейс Ивбемобжектсинк

Интерфейс **ивбемобжектсинк** создает интерфейс приемника, который может получать все типы уведомлений в модели программирования WMI. Клиенты должны реализовать этот интерфейс для получения результатов [асинхронных методов](making-an-asynchronous-call-with-c--.md) [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)и конкретных типов уведомлений о событиях. Поставщики используют, но не реализуют этот интерфейс для предоставления событий и объектов WMI.

Как правило, поставщики вызывают реализацию, предоставляемую WMI. В этих случаях вызовите метод [**указания**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) для предоставления объектов службе WMI. После этого вызовите [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , чтобы обозначить конец последовательности уведомлений. Кроме того, можно вызвать **SetStatus** , чтобы указать ошибки, когда у приемника нет объектов.

При программировании асинхронных клиентов WMI пользователь предоставляет реализацию. Инструментарий WMI вызывает методы для доставки объектов и установки состояния результата.

> [!Note]  
> Если клиентское приложение передает один и тот же интерфейс приемника в два разных перекрывающихся асинхронных вызова, WMI не гарантирует порядок обратного вызова. Клиентские приложения, которые делают перекрывающиеся асинхронные вызовы, должны либо передавать разные объекты-приемник, либо выполнять сериализацию своих вызовов.

 

> [!Note]  
> Поскольку обратный вызов к приемнику может быть не возвращен на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

## <a name="members"></a>Элементы

Интерфейс **ивбемобжектсинк** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивбемобжектсинк** содержит следующие методы.



| Метод                                         | Описание                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Казывая**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Получает объекты уведомлений.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Вызывается источниками для обозначения конца последовательности уведомлений или для отправки приемнику других кодов состояния.<br/> |



 

## <a name="remarks"></a>Комментарии

При реализации приемника подписки на события (**ивбемобжектсинк** или [**ивбемевентсинк**](iwbemeventsink.md)) не следует вызывать WMI из методов [**указания**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) или [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) объекта приемника. Например, вызов [**IWbemServices:: канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) для отмены приемника из реализации [**индикации**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) может повлиять на состояние WMI. Чтобы отменить подписку на события, установите флаг и вызовите **IWbemServices:: канцеласинккалл** из другого потока или объекта. Для реализаций, которые не связаны с приемником событий, например объектом, перечислением и получением запросов, можно выполнить обратный вызов к инструментарию WMI.

Реализации приемника должны обрабатывать уведомление о событии в течение 100 мс, поскольку поток WMI, доставляющий уведомление о событии, не может выполнить другие действия, пока объект приемника не завершит обработку. Если для уведомления требуется большой объем обработки, приемник может использовать внутреннюю очередь для другого потока, чтобы обработать обработку.

## <a name="examples"></a>Примеры

Следующий пример кода является простой реализацией приемника объекта. Этот пример можно использовать с [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) для получения возвращенных экземпляров:


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Вбемкли. h (включение Вбемидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Вбемууид. lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[COM API для WMI](com-api-for-wmi.md)
</dt> <dt>

[Создание асинхронного вызова с помощью C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Получение событий для длительности вашего приложения](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




