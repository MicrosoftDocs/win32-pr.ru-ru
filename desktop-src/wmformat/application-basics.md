---
title: Основные сведения о приложениях
description: Основные сведения о приложениях
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Пакет SDK для формата мультимедиа, основы приложений DRM
- Управление цифровыми правами (DRM), основы приложений
- DRM (Управление цифровыми правами), основы приложений
- Управление цифровыми правами (DRM), функция Вмдрмстартуп
- DRM (Управление цифровыми правами), функция Вмдрмстартуп
- вмдрмстартуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356160565754764ac71cb152799a0fd9d1530e6e6969dc7a56e203b7504645d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086210"
---
# <a name="application-basics"></a>Основные сведения о приложениях

существует дополнительная обработка, которую необходимо выполнить для любого приложения, использующего расширенные api клиента DRM Windows Media. В этом разделе описываются требования для простого приложения.

во-первых, необходимо инициализировать расширенные api клиента DRM Windows Media, вызвав функцию [**вмдрмстартуп**](wmdrmstartup.md) . Объекты пакета SDK являются COM-объектами, но вам не нужно вызывать **коинтиализе**, так как функция **ВМДРМСТАТУП** инициализирует COM для вас.

> [!Note]  
> пакет SDK для Windows media Format использует только подмножество com, поэтому при использовании com-объектов, отличных от тех, которые находятся в расширенном API клиента DRM для Windows Media, необходимо по-прежнему вызывать функцию **coinitialize**.

 

все объекты расширенных api клиента DRM Windows Media создаются с помощью вспомогательных функций и методов. Для создания объекта никогда не нужно вызывать **CoCreateInstance** . Первый интерфейс для создания экземпляра для любого приложения, использующего пакет SDK, — это [**ивмдрмпровидер**](iwmdrmprovider.md), который можно использовать для создания экземпляров всех других базовых интерфейсов. Чтобы получить экземпляр **ивмдрмпровидер**, необходимо вызвать либо [**Вмдрмкреатепровидер**](wmdrmcreateprovider.md) , либо [**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md). Разница между этими функциями заключается в том, что **вмдрмкреатепровидер** создает объект, который, в свою очередь, может создавать только те объекты, которые не поддерживают методы, требующие наличия библиотеки-заглушки.

После создания экземпляра **ивмдрмпровидер** можно создать другие необходимые объекты, вызвав [**Ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).

Когда вы будете готовы выйти из приложения, необходимо освободить ресурсы подсистемы DRM, вызвав функцию [**вмдрмшутдовн**](wmdrmshutdown.md) . Эта функция также завершает работу COM.

в следующем примере кода показано, как инициализировать и завершить приложение, которое использует расширенные api клиента DRM Windows Media.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**начало работы**](drm-getting-started.md)
</dt> </dl>

 

 




