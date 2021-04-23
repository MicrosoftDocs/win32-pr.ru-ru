---
description: Контекст безопасности — это набор атрибутов и правил безопасности, действующих во время сеанса связи.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Семантика контекста SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651044"
---
# <a name="sspi-context-semantics"></a><span data-ttu-id="5cd68-103">Семантика контекста SSPI</span><span class="sxs-lookup"><span data-stu-id="5cd68-103">SSPI Context Semantics</span></span>

<span data-ttu-id="5cd68-104">[*Контекст безопасности*](../secgloss/s-gly.md) — это набор атрибутов и правил безопасности, действующих во время сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="5cd68-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="5cd68-105">Сюда входят такие сведения, как удостоверения участника и сведения о ключах, шифрах и используемых алгоритмах.</span><span class="sxs-lookup"><span data-stu-id="5cd68-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="5cd68-106">Для [*интерфейса поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI) контекст безопасности — это непрозрачная структура, созданная с помощью Exchange, включающей функцию [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) и [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="5cd68-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="5cd68-107">Дополнительные сведения об атрибутах контекста см. в разделе [требования к контексту](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5cd68-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="5cd68-108">Модель SSPI поддерживает три типа контекстов безопасности.</span><span class="sxs-lookup"><span data-stu-id="5cd68-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cd68-109">Тип</span><span class="sxs-lookup"><span data-stu-id="5cd68-109">Type</span></span></th>
<th><span data-ttu-id="5cd68-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5cd68-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5cd68-111"><a href="connection-oriented-contexts.md">Соединение</a></span><span class="sxs-lookup"><span data-stu-id="5cd68-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="5cd68-112"><a href="/windows/desktop/SecGloss/c-gly"><em>Контекст</em></a> , ориентированный на соединение, является наиболее распространенным контекстом безопасности и проще в использовании.</span><span class="sxs-lookup"><span data-stu-id="5cd68-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="5cd68-113">Вызывающий объект отвечает за общий формат сообщений и расположение данных в сообщении.</span><span class="sxs-lookup"><span data-stu-id="5cd68-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="5cd68-114">Вызывающий объект также отвечает за расположение связанных с безопасностью полей в сообщении, например расположение данных подписи.</span><span class="sxs-lookup"><span data-stu-id="5cd68-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cd68-115"><a href="datagram-contexts.md">Datagram</a></span><span class="sxs-lookup"><span data-stu-id="5cd68-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="5cd68-116">Контекст, ориентированный на <a href="/windows/desktop/SecGloss/d-gly"><em>датаграмму</em></a>, обеспечивает дополнительную поддержку связи с датаграммами в стиле DCE.</span><span class="sxs-lookup"><span data-stu-id="5cd68-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="5cd68-117">Его также можно использовать в качестве универсального для транспортного приложения, ориентированного на датаграммы.</span><span class="sxs-lookup"><span data-stu-id="5cd68-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="5cd68-118">Пакет <a href="microsoft-kerberos.md">Microsoft Kerberos</a> не поддерживает контексты датаграмм в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="5cd68-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cd68-119"><a href="stream-contexts.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="5cd68-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="5cd68-120">Поток-ориентированный контекст отвечает за блокировку и форматирование сообщений в пакете безопасности.</span><span class="sxs-lookup"><span data-stu-id="5cd68-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="5cd68-121">Вызывающий объект не заинтересован в форматировании, а вместо необработанного потока данных.</span><span class="sxs-lookup"><span data-stu-id="5cd68-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5cd68-122">См. также</span><span class="sxs-lookup"><span data-stu-id="5cd68-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cd68-123">Требования к контексту</span><span class="sxs-lookup"><span data-stu-id="5cd68-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="5cd68-124">Контексты, ориентированные на соединение</span><span class="sxs-lookup"><span data-stu-id="5cd68-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="5cd68-125">Контексты датаграмм</span><span class="sxs-lookup"><span data-stu-id="5cd68-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="5cd68-126">Контексты потока</span><span class="sxs-lookup"><span data-stu-id="5cd68-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
