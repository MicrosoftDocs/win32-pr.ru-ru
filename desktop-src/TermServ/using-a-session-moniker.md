---
title: Использование моникера сеанса
description: Активация "сеанс — сеанс" позволяет клиентскому процессу активировать локальный серверный процесс в указанном сеансе.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fc5c65c3e2efd3e566a3fdde6982fefe5bb14fbefd98ca8abd335955b7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868854"
---
# <a name="using-a-session-moniker"></a>Использование моникера сеанса

Активация "сеанс — сеанс" позволяет клиентскому процессу активировать локальный серверный процесс в указанном сеансе. Это можно сделать отдельно для каждого сеанса, используя предоставленное системой специальное имя сеанса. Дополнительные сведения о создании моникера сеанса см. в разделе [Активация сеанса между сеансами с моникером сеанса](session-to-session-activation-with-a-session-moniker.md).

В следующем примере показано, как активировать локальный серверный процесс с ИДЕНТИФИКАТОРом класса "10000013-0000-0000-0000-000000000001" в сеансе с ИДЕНТИФИКАТОРом сеанса 3.

Во-первых, пример вызывает [**функцию CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) для инициализации библиотеки COM. Затем пример вызывает [**креатебиндкткс**](/windows/win32/api/objbase/nf-objbase-createbindctx) для получения указателя на реализацию интерфейса [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) . Этот объект хранит сведения об операциях привязки моникера. указатель необходим для вызова методов интерфейса [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) . Затем в примере вызывается функция [мкпарседисплайнамикс](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) для создания моникера составного сеанса, а затем метод [**IMoniker:: биндтубжект**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) для активации соединения между клиентом и сервером, используя только что созданный моникер сеанса. На этом этапе можно использовать указатель интерфейса для выполнения требуемых операций с объектом. Наконец, в примере освобождается контекст привязки и вызывается функция [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



Так как "{идентификатор класса моникера класса}" также является способом именования моникера класса, можно использовать следующую строку для именования составного моникера (моникер сеанса, состоящего из моникера класса), а не способом, приведенным в предыдущем примере.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Если один и тот же пользователь вошел в каждый сеанс во время межсеансовой активации, можно успешно активировать любой серверный процесс, настроенный для запуска в режиме интерактивной активации пользователя с помощью команды RunAs. Если в каждый сеанс входит несколько пользователей, сервер должен вызвать функцию [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы установить соответствующие права пользователя, прежде чем произойдет успешная Активация и подключение между клиентом и сервером. Одним из способов добиться этого является то, что сервер реализует пользовательский интерфейс [**иакцессконтрол**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) и передает реализацию в **CoInitializeSecurity**. В любом случае пользователь клиента должен иметь соответствующие разрешения на [**Запуск**](../com/launchpermission.md) и [**доступ**](../com/accesspermission.md) , указанные в приложении, работающем на сервере. Дополнительные сведения см. [в разделе Безопасность в com](../com/security-in-com.md).

 

Дополнительные сведения о предоставляемых системой моникерах, моникерах и режимах активации см. в разделе [моникеры](../com/monikers.md), интерфейс [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) и [ключ AppID](/windows/desktop/com/appid-key) в документации по com в пакете SDK для платформы.

 

 