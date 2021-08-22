---
title: Подключение к службе BITS
description: Чтобы подключиться к службе BITS, создайте экземпляр объекта Баккграундкопиманажер, как показано в следующем примере.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dacd97b78fa9c5d3a1e410a44e3c376368654e99a6f4ace9161d36b127d9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528944"
---
# <a name="connecting-to-the-bits-service"></a>Подключение к службе BITS

Чтобы подключиться к системной службе BITS, создайте экземпляр объекта Баккграундкопиманажер, как показано в следующем примере. системная служба BITS — это Windowsная системная служба, выполняющаяся на клиентском компьютере, который реализует функцию фоновой передачи.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



Чтобы проверить наличие определенной версии BITS, используйте символьный идентификатор класса для Баккграундкопиманажер в зависимости от версии, которую необходимо проверить. Например, чтобы проверить наличие BITS 10,2, используйте CLSID \_ BackgroundCopyManager10 \_ 2.

В следующем примере показано, как использовать один из символьных идентификаторов классов.


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



Используйте методы интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) для [создания заданий перемещения](creating-a-job.md), [перечисления заданий](enumerating-jobs-in-the-transfer-queue.md) в очереди и [получения заданий](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



Служба BITS требует, чтобы прокси-серверы интерфейса клиента использовали олицетворение или уровень ОЛИЦЕТВОРЕНия. Если приложение не вызывает [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com использует функцию Identify по умолчанию. Служба BITS завершается с ошибкой E \_ ACCESSDENIED, если не задан правильный уровень олицетворения. Если вы предоставляете библиотеку, которая выполняет интерфейсы BITS, и приложение, вызывающее библиотеку, задает уровень олицетворения, приведенный ниже, необходимо вызвать метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) , чтобы задать правильный уровень олицетворения для каждого вызываемого интерфейса BITS.

Перед завершением работы приложения Освободите копию указателя интерфейса [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , как показано в следующем примере.


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Вызов BITS из .NET и C#](/windows/desktop/Bits/bits-dot-net) для BITS
</dt> </dl>

 

 