---
title: API-интерфейс WinRM C++
description: интерфейсы служба удаленного управления Windows могут использоваться для получения данных или управления ресурсами на удаленном компьютере. Этот API предназначен главным образом для внутреннего использования. Вместо этого рекомендуется использовать API-интерфейс оболочки клиента WinRM, если это возможно.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742950"
---
# <a name="winrm-c-api"></a>API-интерфейс WinRM C++

интерфейсы служба удаленного управления Windows могут использоваться для получения данных или управления [*ресурсами*](windows-remote-management-glossary.md) на удаленном компьютере. Этот API предназначен главным образом для внутреннего использования. Вместо этого рекомендуется использовать [API-интерфейс оболочки клиента WinRM](client-shell-api.md) , если это возможно. Интерфейсы в точности соответствуют API- [интерфейсу сценариев WinRM](winrm-scripting-api.md).

Интерфейсы WinRM, которые наследуют непосредственно от **IDispatch** , имеют соответствующий объект скрипта. Дополнительные сведения см. в разделе [API сценариев WinRM](winrm-scripting-api.md).

Для многопоточных приложений WinRM не поддерживает отдельные потоки, обращающиеся к одному и тому же объекту [**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .

WinRM предоставляет следующие интерфейсы.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**ивсман**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Предоставляет методы и свойства, используемые для создания нового сеанса и управления установленным сеансом. [**WSMan**](wsman.md) — это соответствующий объект скрипта.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**ивсманекс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Предоставляет методы и свойства, используемые для создания нового [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator). Этот метод доступен для объекта скрипта [**WSMan**](wsman.md) .

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**ивсманконнектионоптионс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Определяет имя пользователя и пароль, используемые для удаленных соединений. [**ConnectionOptions**](connectionoptions.md) — это соответствующий объект скрипта.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Определяет сетевые операции и свойства, доступные для сеанса. [**Session**](session.md) — это соответствующий объект скрипта.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Представляет коллекцию результатов, возвращенных при перечислении ресурса. [**Перечислитель**](enumerator.md) — это соответствующий объект скрипта.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Предоставляет путь к ресурсу. Вы можете использовать объект [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) вместо [*URI ресурса*](windows-remote-management-glossary.md) в операциях с объектами [**сеанса**](session.md) . [**ResourceLocator**](resourcelocator.md) — это соответствующий объект скрипта.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Справочник по удаленному управлению](windows-remote-management-reference.md)
</dt> </dl>

 

 




