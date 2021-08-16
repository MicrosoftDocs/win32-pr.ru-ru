---
description: Контекст безопасности — это набор атрибутов и правил безопасности, действующих во время сеанса связи.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Семантика контекста SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddadd2c8a76f1fdc151273dca2027b8cb55776a50b78a7c08343c22410ae90e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916983"
---
# <a name="sspi-context-semantics"></a>Семантика контекста SSPI

[*Контекст безопасности*](../secgloss/s-gly.md) — это набор атрибутов и правил безопасности, действующих во время сеанса связи. Сюда входят такие сведения, как удостоверения участника и сведения о ключах, шифрах и используемых алгоритмах. Для [*интерфейса поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI) контекст безопасности — это непрозрачная структура, созданная с помощью Exchange, включающей функцию [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) и [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Дополнительные сведения об атрибутах контекста см. в разделе [требования к контексту](context-requirements.md).

Модель SSPI поддерживает три типа контекстов безопасности.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">Соединение</a></td>
<td><a href="/windows/desktop/SecGloss/c-gly"><em>Контекст</em></a> , ориентированный на соединение, является наиболее распространенным контекстом безопасности и проще в использовании. Вызывающий объект отвечает за общий формат сообщений и расположение данных в сообщении. Вызывающий объект также отвечает за расположение связанных с безопасностью полей в сообщении, например расположение данных подписи.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagram</a></td>
<td>Контекст, ориентированный на <a href="/windows/desktop/SecGloss/d-gly"><em>датаграмму</em></a>, обеспечивает дополнительную поддержку связи с датаграммами в стиле DCE. Его также можно использовать в качестве универсального для транспортного приложения, ориентированного на датаграммы.<br/>
<blockquote>
<p>[!Important]</p>
<p>Пакет <a href="microsoft-kerberos.md">Microsoft Kerberos</a> не поддерживает контексты датаграмм в пользовательском режиме.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Поток-ориентированный контекст отвечает за блокировку и форматирование сообщений в пакете безопасности. Вызывающий объект не заинтересован в форматировании, а вместо необработанного потока данных.<br/></td>
</tr>
</tbody>
</table>



 

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

 

 
