---
title: API сценариев WinRM
description: Служба удаленного управления Windows объекты скрипта реализуются как уровень выше протокола WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700639"
---
# <a name="winrm-scripting-api"></a>API сценариев WinRM

Служба удаленного управления Windows объекты скрипта реализуются как слой над [протокол WS-Management](ws-management-protocol.md). Объекты скрипта позволяют получать данные или управлять [*ресурсами*](windows-remote-management-glossary.md) на локальных и удаленных компьютерах.

## <a name="ws-management-objects"></a>WS-Management объекты

Каждый объект скрипта имеет соответствующий интерфейс C++. Дополнительные сведения см. в разделе [WinRM C++ API](winrm-c---api.md) и [сценарии в Служба удаленного управления Windows](scripting-in-windows-remote-management.md).

В API-интерфейсах сценариев WinRM предоставляются следующие объекты.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Определяет имя пользователя и пароль, используемые для удаленных соединений. Имя пользователя и пароль передаются при вызове метода [**креатеконнектионоптионс**](wsman-createconnectionoptions.md) . Дополнительные сведения см. в разделе [Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md). Соответствующий интерфейс C++ — [**ивсманконнектионоптионс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Перечислитель**](enumerator.md)
</dt> <dd>

Представляет коллекцию результатов, возвращенных при перечислении ресурса. Дополнительные сведения см. [в разделе перечисление или вывод всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md). Соответствующий интерфейс C++ — [**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Предоставляет путь к ресурсу. Вместо [*URI ресурса*](windows-remote-management-glossary.md) в операциях объекта [**сеанса**](session.md) можно использовать объект [**ResourceLocator**](resourcelocator.md) , например [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md). Соответствующий интерфейс C++ — [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Сессии**](session.md)
</dt> <dd>

Определяет сетевые операции и свойства, доступные для сеанса, такие как [**сеанс. Get**](session-get.md), [**сеанс. Перечисление**](session-enumerate.md), [**сеанс. Invoke**](session-invoke.md). Дополнительные сведения см. [в разделе Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md). Соответствующий интерфейс C++ — [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**Ведущий**](wsman.md)
</dt> <dd>

Предоставляет методы и свойства, используемые для создания нового сеанса или управления установленным сеансом. Дополнительные сведения см. в разделе [использование служба удаленного управления Windows](using-windows-remote-management.md). Соответствующими интерфейсами C++ являются [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) и [**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Справочник по служба удаленного управления Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




