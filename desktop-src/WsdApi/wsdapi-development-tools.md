---
description: Средства разработки WSDAPI, включенные в Windows SDK (WSD CodeGen, узел отладки WSD и клиент отладки WSD), позволяют разработчикам создавать и отлаживать клиенты и устройства на основе WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Средства разработки WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701931"
---
# <a name="wsdapi-development-tools"></a>Средства разработки WSDAPI

Средства разработки WSDAPI, включенные в Windows SDK (WSD CodeGen, узел отладки WSD и клиент отладки WSD), позволяют разработчикам создавать и отлаживать клиенты и устройства на основе WSDAPI. Исходный код для этих средств недоступен. Средства пакета SDK находятся в следующем каталоге: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) преобразует контракт WSDL в созданный код C++, который разработчики могут вызывать напрямую в. Он обрабатывает представление сериализации данных и подключения, чтобы разработчики могли сосредоточиться на проектировании приложений. Дополнительные сведения о CodeGenе WSD см. [в разделе веб-службы на устройствах генератор кода](web-services-for-devices-code-generator.md). Это средство доступно в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows и в комплекте драйверов для Windows (WDK).

Средства отладки сервера WSD (всддебуг \_host.exe) и клиент отладки WSD (всддебуг \_client.exe) помогают разработчикам в отладке своих клиентов и узлов. Эти средства можно использовать для проверки и проверки WS-Discovery и трафика обмена метаданными. Дополнительные сведения об узле отладки WSD и клиенте отладки WSD см. в разделе [средства отладки](debugging-tools.md). Эти средства доступны только в Windows SDK.

Существует дополнительное средство разработки с именем " [основной инструмент взаимодействия WSDAPI (всдбит)](https://msdn.microsoft.com/library/cc264250.aspx)", которое доступно только в WDK. Это средство используется для тестирования методов служб, механизма оптимизации передачи сообщений (MTOM), вложений или WS-Eventing.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разработка приложений WSD в Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Генератор кода для веб-служб на устройствах](web-services-for-devices-code-generator.md)
</dt> <dt>

[Базовое средство взаимодействия WSDAPI (ВСДБИТ)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Средства отладки](debugging-tools.md)
</dt> </dl>

 

 



