---
title: Интерфейсы поставщика протокол удаленного рабочего стола
description: Интерфейсы, поддерживаемые API поставщика протокол удаленного рабочего стола.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bde36cb70f937559dce20a73a485ec109a2cf6c6ae6c687655963c70e6ce22b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681234"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Интерфейсы поставщика протокол удаленного рабочего стола

API поставщика протокол удаленного рабочего стола поддерживает следующие интерфейсы.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**иврдспротоколконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Предоставляет методы, вызываемые службой службы удаленных рабочих столов для настройки клиентского соединения.

</dd> <dt>

[**иврдспротоколконнектионкаллбакк**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Предоставляет методы, предоставляющие сведения о состоянии клиентского соединения и выполняющие действия для клиента. Этот интерфейс реализуется службой службы удаленных рабочих столов и вызывается протоколом.

</dd> <dt>

[**иврдспротоколлиценсеконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Предоставляет методы, используемые службой службы удаленных рабочих столов для выполнения подтверждения лицензирования во время последовательности подключения.

</dd> <dt>

[**иврдспротоколлистенер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Предоставляет методы, запрашивающие запуск и прекращение прослушивания протоколом запросов на подключение клиента.

</dd> <dt>

[**иврдспротоколлистенеркаллбакк**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Предоставляет методы, уведомляющие службу службы удаленных рабочих столов, к которой подключен клиент.

</dd> <dt>

[**иврдспротоколлогонеррорредиректор**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Предоставляет методы, вызываемые службой службы удаленных рабочих столов для обновления состояния входа в систему и определения способа направления сообщений об ошибках входа в систему.

</dd> <dt>

[**иврдспротоколманажер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Предоставляет методы, которые служба службы удаленных рабочих столов использует для взаимодействия с поставщиком протокола.

</dd> <dt>

[**иврдспротоколсеттингс**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Предоставляет методы для извлечения и добавления параметров, связанных с политикой.

</dd> <dt>

[**иврдспротоколшадовкаллбакк**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Предоставляет методы, вызываемые протоколом, для уведомления службы службы удаленных рабочих столов о запуске или прекращении целевой стороны тени.

</dd> <dt>

[**иврдспротоколшадовконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Предоставляет методы, уведомляющие поставщика протокола о состоянии теневого сеанса.

</dd> <dt>

[**иврдсремотефксграфиксконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Предоставляет методы, относящиеся к манипуляции и пониманию графики в клиентском подключении.

</dd> <dt>

[Нерекомендуемые интерфейсы поставщика протокола рабочего стола](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Следующие интерфейсы являются устаревшими и больше не должны использоваться. Для новых проектов вместо этого используйте интерфейсы интерфейсов поставщика протокол удаленного рабочего стола.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по поставщику протокол удаленного рабочего стола](custom-remote-protocol-reference.md)
</dt> <dt>

[Перечисления поставщика протокол удаленного рабочего стола](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Структуры поставщика протокол удаленного рабочего стола](custom-remote-protocol-structures.md)
</dt> <dt>

[Объединения поставщиков протокол удаленного рабочего стола](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




