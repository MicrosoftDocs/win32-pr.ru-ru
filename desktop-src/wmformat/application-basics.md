---
title: Основные сведения о приложениях
description: Основные сведения о приложениях
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media Format SDK, основы приложений DRM
- Управление цифровыми правами (DRM), основы приложений
- DRM (Управление цифровыми правами), основы приложений
- Управление цифровыми правами (DRM), функция Вмдрмстартуп
- DRM (Управление цифровыми правами), функция Вмдрмстартуп
- вмдрмстартуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252824"
---
# <a name="application-basics"></a>Основные сведения о приложениях

Существует дополнительная обработка, которую необходимо выполнить для любого приложения, использующего расширенные API клиента DRM Windows Media. В этом разделе описываются требования для простого приложения.

Во-первых, необходимо инициализировать расширенные API клиента DRM Windows Media, вызвав функцию [**вмдрмстартуп**](wmdrmstartup.md) . Объекты пакета SDK являются COM-объектами, но вам не нужно вызывать **коинтиализе**, так как функция **ВМДРМСТАТУП** инициализирует COM для вас.

> [!Note]  
> Пакет SDK для формата Windows Media использует только подмножество COM, поэтому при использовании COM-объектов, отличных от тех, которые находятся в расширенном API клиента DRM Windows Media, необходимо по-прежнему вызывать функцию **CoInitialize**.

 

Все объекты расширенных API клиента DRM Windows Media создаются с помощью вспомогательных функций и методов. Для создания объекта никогда не нужно вызывать **CoCreateInstance** . Первый интерфейс для создания экземпляра для любого приложения, использующего пакет SDK, — это [**ивмдрмпровидер**](iwmdrmprovider.md), который можно использовать для создания экземпляров всех других базовых интерфейсов. Чтобы получить экземпляр **ивмдрмпровидер**, необходимо вызвать либо [**Вмдрмкреатепровидер**](wmdrmcreateprovider.md) , либо [**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md). Разница между этими функциями заключается в том, что **вмдрмкреатепровидер** создает объект, который, в свою очередь, может создавать только те объекты, которые не поддерживают методы, требующие наличия библиотеки-заглушки.

После создания экземпляра **ивмдрмпровидер** можно создать другие необходимые объекты, вызвав [**Ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).

Когда вы будете готовы выйти из приложения, необходимо освободить ресурсы подсистемы DRM, вызвав функцию [**вмдрмшутдовн**](wmdrmshutdown.md) . Эта функция также завершает работу COM.

В следующем примере кода показано, как инициализировать и завершить приложение, которое использует расширенные API клиента DRM Windows Media.


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**начало работы**](drm-getting-started.md)
</dt> </dl>

 

 




