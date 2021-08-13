---
description: Если веб-служба XML, к которой нужно получить доступ, была создана путем предоставления доступа к приложению COM+, рассмотрите возможность доступа к нему в режиме активируемого клиентом объекта (Као), что позволяет избежать создания прокси-сервера во время выполнения и повысить производительность с помощью постоянных соединений.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Доступ к веб-службам XML в режиме Као
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3f8dc1fa3c037d03d8b69cf45737c7211d92f7d38e733a97b9be109a2243a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549466"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Доступ к веб-службам XML в режиме Као

Если веб-служба XML, к которой нужно получить доступ, была создана путем предоставления доступа к приложению COM+, рассмотрите возможность доступа к нему в режиме активируемого клиентом объекта (Као), что позволяет избежать создания прокси-сервера во время выполнения и повысить производительность с помощью постоянных соединений. Чтобы получить доступ к веб-службе XML в режиме Као, сначала [экспортируйте](exporting-a-soap-enabled-application.md) соответствующее приложение с поддержкой SOAP с сервера в режиме прокси-сервера, а затем [импортируйте](importing-a-soap-enabled-application.md) приложение в клиент, из которого вы хотите получить доступ к приложению как к веб-службе XML. Затем на клиенте можно создать экземпляры компонентов приложения так же, как компоненты локальных приложений, например с помощью **GetObject** и [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Пользовательский интерфейс

Не применяется.

## <a name="visual-basic"></a>Visual Basic

в следующем Visual Basic фрагменте кода показано использование компонента приложения COM+, доступного в виде веб-службы XML в режиме као.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

В следующем фрагменте кода показано использование компонента приложения COM+, доступного в виде веб-службы XML, в режиме Као.


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Доступ к веб-службам XML в режиме ВКО](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Общие сведения о службе COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Создание веб-служб XML](creating-xml-web-services.md)
</dt> <dt>

[Защита веб-служб XML](securing-xml-web-services.md)
</dt> </dl>

 

 
