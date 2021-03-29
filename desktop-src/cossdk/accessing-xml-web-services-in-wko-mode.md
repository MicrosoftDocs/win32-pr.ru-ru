---
description: Можно получить доступ к любой веб-службе XML и использовать ее, даже если эта веб-служба XML не была создана с помощью COM+ или даже Microsoft Windows, при условии, что веб-служба XML публикует описание синтаксиса WSDL.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Доступ к веб-службам XML в режиме ВКО
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807295"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Доступ к веб-службам XML в режиме ВКО

Можно получить доступ к любой веб-службе XML и использовать ее, даже если эта веб-служба XML не была создана с помощью COM+ или даже Microsoft Windows, при условии, что веб-служба XML публикует описание синтаксиса WSDL. Просто создайте экземпляр компонента с помощью моникера SOAP: WSDL = URL, где URL — это URL-адрес описания языка WSDL XML Web Service, к которому требуется получить доступ. Это режим хорошо известного объекта (ВКО) для доступа к веб-службам XML.

Методы объекта могут вызываться без каких бы то ни было особых соображений. Доступ к веб-службе XML осуществляется через запрос SOAP, и ответ интерпретируется прозрачно.

## <a name="component-services-administrative-tool"></a>Средство администрирования служб компонентов

Не применяется.

## <a name="visual-basic"></a>Visual Basic

В следующем фрагменте кода Microsoft Visual Basic показано использование веб-службы XML в режиме ВКО.


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

## <a name="remarks"></a>Комментарии

При первом обращении к веб-службе XML в режиме ВКО COM+ создает прокси-клиент и компилирует его в фоновый режим. Это поколение времени выполнения и отсутствие постоянных подключений в режиме ВКО значительно снижают производительность в сравнении с режимом Као.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Доступ к веб-службам XML в режиме Као](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Общие сведения о службе COM+ SOAP](com--soap-service-overview.md)
</dt> <dt>

[Создание веб-служб XML](creating-xml-web-services.md)
</dt> <dt>

[Защита веб-служб XML](securing-xml-web-services.md)
</dt> </dl>

 

 



