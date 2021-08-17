---
title: API сценариев WinRM
description: Windows Объекты сценариев удаленного управления реализуются как слой над протоколом WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742762"
---
# <a name="winrm-scripting-api"></a>API сценариев WinRM

Windows Объекты сценариев удаленного управления реализуются как слой над [протокол WS-Management](ws-management-protocol.md). Объекты скрипта позволяют получать данные или управлять [*ресурсами*](windows-remote-management-glossary.md) на локальных и удаленных компьютерах.

## <a name="ws-management-objects"></a>WS-Management объекты

Каждый объект скрипта имеет соответствующий интерфейс C++. дополнительные сведения см. в разделе [WinRM C++ API](winrm-c---api.md) и [сценарии в служба удаленного управления Windows](scripting-in-windows-remote-management.md).

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

Предоставляет методы и свойства, используемые для создания нового сеанса или управления установленным сеансом. дополнительные сведения см. в разделе [использование служба удаленного управления Windows](using-windows-remote-management.md). Соответствующими интерфейсами C++ являются [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) и [**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[о служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows Справочник по удаленному управлению](windows-remote-management-reference.md)
</dt> </dl>

 

 




