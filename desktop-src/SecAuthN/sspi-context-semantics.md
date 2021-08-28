---
description: Контекст безопасности — это набор атрибутов и правил безопасности, действующих во время сеанса связи.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Семантика контекста SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423ce097d1ab71cf50983285f3ca8731497ed5a9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482540"
---
# <a name="sspi-context-semantics"></a>Семантика контекста SSPI

[*Контекст безопасности*](../secgloss/s-gly.md) — это набор атрибутов и правил безопасности, действующих во время сеанса связи. Сюда входят такие сведения, как удостоверения участника и сведения о ключах, шифрах и используемых алгоритмах. Для [*интерфейса поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI) контекст безопасности — это непрозрачная структура, созданная с помощью Exchange, включающей функцию [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) и [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Дополнительные сведения об атрибутах контекста см. в разделе [требования к контексту](context-requirements.md).

Модель SSPI поддерживает три типа контекстов безопасности.




| Тип | Описание | 
|------|-------------|
| <a href="connection-oriented-contexts.md">Соединение</a> | <a href="/windows/desktop/SecGloss/c-gly"><em>Контекст</em></a> , ориентированный на соединение, является наиболее распространенным контекстом безопасности и проще в использовании. Вызывающий объект отвечает за общий формат сообщений и расположение данных в сообщении. Вызывающий объект также отвечает за расположение связанных с безопасностью полей в сообщении, например расположение данных подписи.<br /> | 
| <a href="datagram-contexts.md">Datagram</a> | Контекст, ориентированный на <a href="/windows/desktop/SecGloss/d-gly"><em>датаграмму</em></a>, обеспечивает дополнительную поддержку связи с датаграммами в стиле DCE. Его также можно использовать в качестве универсального для транспортного приложения, ориентированного на датаграммы.<br /><blockquote><p>[!Important]</p><p>Пакет <a href="microsoft-kerberos.md">Microsoft Kerberos</a> не поддерживает контексты датаграмм в пользовательском режиме.<br /></p></blockquote><br /> | 
| <a href="stream-contexts.md">STREAM</a> | Поток-ориентированный контекст отвечает за блокировку и форматирование сообщений в пакете безопасности. Вызывающий объект не заинтересован в форматировании, а вместо необработанного потока данных.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Требования к контексту](context-requirements.md)
</dt> <dt>

[Контексты, ориентированные на соединение](connection-oriented-contexts.md)
</dt> <dt>

[Контексты датаграмм](datagram-contexts.md)
</dt> <dt>

[Контексты потока](stream-contexts.md)
</dt> </dl>

 

 
