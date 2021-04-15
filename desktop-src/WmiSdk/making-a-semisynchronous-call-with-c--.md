---
description: 'Вызовы семисинчронаус являются рекомендуемыми средствами для вызова методов WMI, таких как IWbemServices:: ExecMethod и методы поставщика, например метода chkdsk \_ класса Win32 LogicalDisk.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Вызов Семисинчронаус с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546178"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Вызов Семисинчронаус с помощью C++

Вызовы семисинчронаус являются рекомендуемыми средствами для вызова методов WMI, таких как [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) и методы поставщика, например [**метода chkdsk \_ класса Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

Одной из недостатков синхронной обработки является то, что вызывающий поток блокируется до завершения вызова. Блокирование может вызвать задержку во время обработки. В отличие от этого, асинхронный вызов должен реализовывать [**свбемсинк**](swbemsink.md) в скрипте. В C++ асинхронный код должен реализовывать интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) , использовать несколько потоков и управлять потоком информации обратно вызывающему объекту. Например, большие результирующие наборы из запросов могут потребовать значительного времени для доставки и принудительного выполнения вызывающей стороны значительных системных ресурсов для выполнения доставки.

Семисинчронаус обработка позволяет разрешать проблемы с блокированием потока и неуправляемой доставкой, опрашивая Специальный объект состояния, реализующий интерфейс [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) . С помощью **ивбемкаллресулт** можно повысить скорость и эффективность запросов, перечислений и уведомлений о событиях.

Следующая процедура описывает, как выполнить вызов семисинчронаус с помощью интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

**Вызов семисинчронаус с помощью интерфейса IWbemServices**

1.  Сделайте вызов обычным, но с флагом WBEM в параметре *ифлагс* установлен флаг **\_ \_ \_ немедленной** установки.

    **Флаг WBEM можно использовать \_ \_ \_ сразу же** , с другими флагами, допустимыми для конкретного метода. Например, для всех вызовов, возвращающих перечислители, следует использовать флаг **WBEM \_ \_ \_ только вперед** . Установка этих флагов в сочетании экономит время и пространство и повышает скорость реагирования.

2.  Опрос результатов.

    При вызове метода, возвращающего перечислитель, например [**IWbemServices:: креатеклассенум**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) или [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), можно опрашивать перечислители с помощью методов [**Иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) или [**иенумвбемклассобжект:: некстасинк**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) . Вызов **иенумвбемклассобжект:: некстасинк** не блокируется и возвращается немедленно. В фоновом режиме Инструментарий WMI начинает доставлять запрошенное число объектов путем вызова [**ивбемобжектсинк:: обозначают**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). Затем WMI останавливается и ожидает другого вызова **некстасинк** .

    При вызове метода, который не возвращает перечислитель, например [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), необходимо задать для параметра *ппкаллресулт* допустимый указатель. Используйте [**ивбемкаллресулт:: жеткаллстатус**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) в возвращенном указателе, чтобы **получить \_ WBEM \_ без \_ ошибок**.

3.  Завершите звонок.

    Для вызова, возвращающего перечислитель, WMI вызывает [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , чтобы сообщить о завершении операции. Если не требуется весь результат, выпустите перечислитель, вызвав метод [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Вызов результатов **выпуска** в WMI отменяет доставку всех оставшихся объектов.

    Для вызова, который не использует перечислитель, извлеките объект [**жеткаллстатус**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) через параметр *плстатус* метода.

В примере кода C++ в этом разделе \# для правильной компиляции требуются следующие операторы include.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



В следующем примере кода показано, как выполнить вызов семисинчронаус для [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

 
