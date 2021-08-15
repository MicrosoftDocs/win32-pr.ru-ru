---
description: можно получить доступ к любой веб-службе xml и использовать ее, даже если эта веб-служба xml не была создана с помощью COM+ или даже Microsoft Windows, при условии, что веб-служба xml публикует описание синтаксиса WSDL.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Доступ к веб-службам XML в режиме ВКО
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f412a1ec6493e713d2635136b2c4e82063cde56c30358653e476f300ffd2ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129406"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Доступ к веб-службам XML в режиме ВКО

можно получить доступ к любой веб-службе xml и использовать ее, даже если эта веб-служба xml не была создана с помощью COM+ или даже Microsoft Windows, при условии, что веб-служба xml публикует описание синтаксиса WSDL. Просто создайте экземпляр компонента с помощью моникера SOAP: WSDL = URL, где URL — это URL-адрес описания языка WSDL XML Web Service, к которому требуется получить доступ. Это режим хорошо известного объекта (ВКО) для доступа к веб-службам XML.

Методы объекта могут вызываться без каких бы то ни было особых соображений. Доступ к веб-службе XML осуществляется через запрос SOAP, и ответ интерпретируется прозрачно.

## <a name="component-services-administrative-tool"></a>Средство администрирования служб компонентов

Не применяется.

## <a name="visual-basic"></a>Visual Basic

в следующем фрагменте кода Microsoft Visual Basic показано использование веб-службы XML в режиме вко.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



В этом фрагменте кода, который иллюстрирует использование компонента приложения COM+, предоставленного в виде веб-службы XML, ServerName — полное доменное имя сервера, на котором размещается веб-служба XML. vroot — это виртуальный корневой каталог IIS, из которого предоставляется веб-служба XML; и progID — это ProgID компонента, который вы хотите использовать.

## <a name="cc"></a>C/C++

В следующем фрагменте кода показано использование веб-службы XML в режиме ВКО.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



В этом фрагменте кода, который иллюстрирует использование компонента приложения COM+, предоставленного в виде веб-службы XML, ServerName — полное доменное имя сервера, на котором размещается веб-служба XML. vroot — это виртуальный корневой каталог IIS, из которого предоставляется веб-служба XML; и progID — это ProgID компонента, который вы хотите использовать.

## <a name="remarks"></a>Remarks

При первом обращении к веб-службе XML в режиме ВКО COM+ создает прокси-клиент и компилирует его в фоновый режим. Это поколение времени выполнения и отсутствие постоянных подключений в режиме ВКО значительно снижают производительность в сравнении с режимом Као.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Доступ к веб-службам XML в режиме Као](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Общие сведения о службе COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Создание веб-служб XML](creating-xml-web-services.md)
</dt> <dt>

[Защита веб-служб XML](securing-xml-web-services.md)
</dt> </dl>

 

 



