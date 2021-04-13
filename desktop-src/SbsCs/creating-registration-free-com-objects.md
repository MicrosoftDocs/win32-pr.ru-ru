---
description: Контексты активации позволяют использовать COM-объекты без необходимости их регистрации.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Создание Registration-Free COM-объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647447"
---
# <a name="creating-registration-free-com-objects"></a>Создание Registration-Free COM-объектов

Контексты активации позволяют использовать COM-объекты без необходимости их регистрации. Это позволяет приложению иметь несколько компонентов с разными функциональными возможностями на основе их версии, а не их данных реестра. Несколько компонентов могут предоставлять один и тот же COM-объект с одним и тем же идентификатором GUID, но иметь различные функциональные возможности, основанные на версии.

Когда приложение запрашивает GUID из [**клсидфромпрогид**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), com сначала выполняет поиск сопоставления от ProgID к CLSID в активном контексте активации. Когда приложение использует [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения указателя на интерфейс экземпляра, com выполняет поиск в активном контексте активации, чтобы найти библиотеку DLL, в которой будет размещен CLSID. Если контекст активации не содержит нужных сведений, COM выполняет поиск сведений в реестре с помощью обычного метода.

Обратите внимание, что поскольку контексты активации относятся к потокам, COM маршалирует контекст активации создания потока на хост-поток и активирует его перед вызовом [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) в потоке узла. Эта функция уже существует в Windows, клиентский код не требуется для реализации этого.

Классы COM можно экспортировать с помощью размещенных компонентов, не провлекая реестр. Несколько компонентов могут предоставлять один и тот же идентификатор ProgID для различных COM-объектов, и приложение размещения должно найти правильный контекст активации, а затем использовать [**клсидфромпрогид**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения указателей на интерфейс размещаемого объекта.

 

 
