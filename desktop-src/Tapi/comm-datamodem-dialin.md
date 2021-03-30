---
description: канал связи/модем/Dial
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: канал связи/модем/Dial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb66d72b5d9f2c75af361153d46f5cac9abdfd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998996"
---
# <a name="commdatamodemdialin"></a>канал связи/модем/Dial

Класс устройств **связи/Dataport/Dialin** состоит из модемных устройств, используемых только для входящих вызовов. Этот класс заменяет класс [**com/Modem**](comm-datamodem.md) в операционных системах Windows 2000 и более поздних версий.

До Windows 2000 в Unimodem TSP поддерживается только класс устройства связи [**/Dataport**](comm-datamodem.md) . Непредвиденное поведение может возникнуть, когда приложение, вызывающее исходящий вызов, изменяет набор конфигураций службой, ожидающей входящего вызова. В приложениях, использующих операционные системы Windows 2000 и более поздних версий, следует указать в вызовах [**линеконфигдиалог**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) или [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)протоколы взаимодействия, **модема, удаленного доступа или связи** [**/модема**](comm-datamodem-dialout.md) . Это позволяет Unimodem поддерживать конфигурацию входящих звонков независимо от конфигурации удаленного доступа.

Несмотря на то, что в Windows 2000 и более поздних версиях используется **канал связи/модем/Dial** , он также может использоваться другими специалистами на любой платформе. Приложения, которые должны выполняться на всех платформах, должны сначала использовать интерфейс **связи/модем/Dial** в вызовах API, требующих класс устройства, и использовать только интерфейс [**Dataport и модем**](comm-datamodem.md) , если API возвращает **линирр \_ инвалкаллстате**.

Поставщик услуг Unimodem преобразует класс устройства связи/ [**Dataport**](comm-datamodem.md) в вызовы [**линеконфигдиалог**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) и [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) в **канал связи, модем/Dial** /Call [**/Dataport/модем/Dial**](comm-datamodem-dialout.md) :

-   Windows 2000 и более поздние версии:
    -   Если в параметре *лпсздевицекласс* в вызове [**Линеконфигдиалог**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)задано **значение NULL** , то для Unimodem предполагается **связь/модем/Dial**. Если в вызове **линеконфигдиалог** указан интерфейс связи [**/Dataport**](comm-datamodem.md) или [**TAPI/Line**](tapi-line.md) , Unimodem преобразует это в [**канал связи/модем/Dial**](comm-datamodem-dialout.md).
    -   В вызове [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) или [**линежетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)объект связи [**/Dataport**](comm-datamodem.md) обрабатывается как [**канал связи, модем или вызов**](comm-datamodem-dialout.md). **Значение NULL** указывает на недопустимый класс устройства.
-   До Windows 2000:
    -   Если в [**линеконфигдиалог**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)указана **null** или [**TAPI/Line**](tapi-line.md) , то для Unimodem предполагается [**канал связи/Dataport**](comm-datamodem.md).

В классе **связи/модема/номеронабирателя** используются структуры и конфигурации, описанные в разделе класс устройств для связи [**и модема**](comm-datamodem.md) .

 

 



