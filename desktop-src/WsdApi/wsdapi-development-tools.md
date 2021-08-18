---
description: средства разработки WSDAPI, включенные в Windows SDK (wsd CodeGen, узел отладки wsd и клиент отладки wsd), позволяют разработчикам создавать и отлаживать клиенты и устройства на основе wsdapi.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Средства разработки WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdad2d87ffafc337c98743f67ae022eb4d1d11616ac42940157a5785066645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130586"
---
# <a name="wsdapi-development-tools"></a>Средства разработки WSDAPI

средства разработки WSDAPI, включенные в Windows SDK (wsd CodeGen, узел отладки wsd и клиент отладки wsd), позволяют разработчикам создавать и отлаживать клиенты и устройства на основе wsdapi. Исходный код для этих средств недоступен. Средства пакета SDK находятся в следующем каталоге: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) преобразует контракт WSDL в созданный код C++, который разработчики могут вызывать напрямую в. Он обрабатывает представление сериализации данных и подключения, чтобы разработчики могли сосредоточиться на проектировании приложений. Дополнительные сведения о CodeGenе WSD см. [в разделе веб-службы на устройствах генератор кода](web-services-for-devices-code-generator.md). это средство доступно в пакете Microsoft Windows Software Development kit (SDK) и в комплекте Windows Driver kit (WDK).

Средства отладки сервера WSD (всддебуг \_host.exe) и клиент отладки WSD (всддебуг \_client.exe) помогают разработчикам в отладке своих клиентов и узлов. Эти средства можно использовать для проверки и проверки WS-Discovery и трафика обмена метаданными. Дополнительные сведения об узле отладки WSD и клиенте отладки WSD см. в разделе [средства отладки](debugging-tools.md). эти средства доступны только в Windows SDK.

Существует дополнительное средство разработки с именем " [основной инструмент взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx)", которое доступно только в WDK. Это средство используется для тестирования методов служб, механизма оптимизации передачи сообщений (MTOM), вложений или WS-Eventing.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка приложений WSD на Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Генератор кода для веб-служб на устройствах](web-services-for-devices-code-generator.md)
</dt> <dt>

[Базовое средство взаимодействия WSDAPI (ВСДБИТ)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Средства отладки](debugging-tools.md)
</dt> </dl>

 

 



