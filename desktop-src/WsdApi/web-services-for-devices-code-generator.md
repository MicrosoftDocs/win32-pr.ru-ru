---
description: Служебная программа командной строки, которая создает программный код из описания службы.
ms.assetid: 76dffca8-bb84-4384-a9e8-120a4cf2acac
title: Генератор кода для веб-служб на устройствах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214fd51468dd3cf46c2625ae0e493851ef90f38b7fea0f64a3973f068be5253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119382274"
---
# <a name="web-services-on-devices-code-generator"></a>Генератор кода для веб-служб на устройствах

Генератор кода веб-служб на устройствах Всдкодежен — это служебная программа командной строки, которая создает программный код из описания службы. Описание службы хранится в файлах WSDL и (или) XSD. Всдкодежен создает файлы C++ и IDL (язык определения интерфейса). Разработчики могут использовать Всдкодежен для создания приложений WSDAPI, не беспокоясь о том, как данные маршалируются и представлены в сети.

Всдкодежен можно использовать для создания кода для службы, клиента или и того и другого. Программа создает код-заглушку для служб, код прокси для клиентов, а также интерфейс и код типа для обоих типов.

это средство доступно в пакете Microsoft Windows Software Development kit (SDK) и в комплекте Windows Driver kit (WDK). Средства пакета SDK находятся в следующем каталоге: <Windows SDK Install Folder> \\ bin.

в Windows SDK содержится пример кода, создаваемого всдкодежен. Дополнительные сведения см. в разделе [примеры WSDAPI](wsdapi-samples.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О Всдкодежен](about-wsdcodegen.md)
</dt> <dt>

[Использование Всдкодежен](using-wsdcodegen.md)
</dt> <dt>

[Справочник по Всдкодежен](wsdcodegen-reference.md)
</dt> <dt>

[Разработка приложений WSD на Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



