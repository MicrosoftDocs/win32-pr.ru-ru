---
title: Справочник по интерфейсу NDR для RPC
description: Отчет о недоставке Microsoft RPC в настоящее время поддерживает следующие функции и структуры
ms.assetid: 2EBB2DD6-60DD-4C9F-9F79-231383B28517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a802720c584d08112c733135c3bb5640e7679c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338396"
---
# <a name="rpc-ndr-interface-reference"></a>Справочник по интерфейсу NDR для RPC

Отчет о недоставке Microsoft RPC в настоящее время поддерживает следующие функции и структуры:

-   [**Кстдстуббуффер \_ AddRef**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_addref)
-   [**Кстдстуббуффер \_ подключение**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_connect)
-   [**Кстдстуббуффер \_ каунтрефс**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_countrefs)
-   [**Кстдстуббуффер \_ дебугсерверкуеринтерфаце**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverqueryinterface)
-   [**Кстдстуббуффер \_ дебугсерверрелеасе**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverrelease)
-   [**Кстдстуббуффер \_ Отключение**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_disconnect)
-   [**Кстдстуббуффер \_ Invoke**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_invoke)
-   [**Кстдстуббуффер \_ исиидсуппортед**](/windows/desktop/api/RpcProxy/nf-rpcproxy-cstdstubbuffer_isiidsupported)
-   [**Кстдстуббуффер \_ QueryInterface**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_queryinterface)
-   [**\_ \_ Прокси-сервер AddRef для IUnknown**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_addref_proxy)
-   [**\_ \_ Прокси-сервер QueryInterface для IUnknown**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**\_ \_ Прокси-сервер выпуска IUnknown**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**ндрасинкклиенткалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrasyncclientcall)
-   [**ндрклеараутпараметерс**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclearoutparameters)
-   [**ндрклиенткалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall)
-   [**NdrClientCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall2)
-   [**ндрконформантаррайунмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarrayunmarshall)
-   [**ндрконформантстрингбуфферсизе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringbuffersize)
-   [**ндрконформантстрингмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringmarshall)
-   [**ндрконформантстрингунмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringunmarshall)
-   [**ндрконтекссандлеинитиализе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandleinitialize)
-   [**ндрконтекссандлесизе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlesize)
-   [**ндрконтекссандлемеморисизе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlememorysize)
-   [**ндрконверт**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconvert)
-   [**\_Выпуск ндркстдстуббуффер**](/previous-versions/aa374242(v=vs.80))
-   [**\_Выпуск NdrCStdStubBuffer2**](/previous-versions/aa374240(v=vs.80))
-   [**ндрдллканунлоаднов**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllcanunloadnow)
-   [**ндрдллжетклассобжект**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllgetclassobject)
-   [**ндрдллрегистерпрокси**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllregisterproxy)
-   [**ндрдллунрегистерпрокси**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllunregisterproxy)
-   [**ндржетусермаршалинфо**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
-   [**ндринтерфацепоинтербуфферсизе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerbuffersize)
-   [**ндринтерфацепоинтерфри**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerfree)
-   [**ндринтерфацепоинтермаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointermarshall)
-   [**ндринтерфацепоинтерунмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerunmarshall)
-   [**ндролеаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndroleallocate)
-   [**ндролефри**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrolefree)
-   [**ндрпоинтербуфферсизе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerbuffersize)
-   [**ндрпоинтерфри**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerfree)
-   [**ндрпоинтермаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointermarshall)
-   [**ндрпоинтерунмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerunmarshall)
-   [**ндрпроксеррорхандлер**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyerrorhandler)
-   [**ндрпроксифрибуффер**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyfreebuffer)
-   [**ндрпроксижетбуффер**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxygetbuffer)
-   [**ндрпроксинитиализе**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyinitialize)
-   [**ндрпроксисендрецеиве**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxysendreceive)
-   [**ндрсимплетипемаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypemarshall)
-   [**ндрсимплетипеунмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypeunmarshall)
-   [**NdrStubCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrstubcall2)
-   [**ндрстубфорвардингфунктион**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubforwardingfunction)
-   [**ндрстубжетбуффер**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubgetbuffer)
-   [**ндрстубинитиализе**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubinitialize)
-   [**ндрусермаршалбуфферсизе**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalbuffersize)
-   [**ндрусермаршалфри**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalfree)
-   [**ндрусермаршалмаршалл**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalmarshall)
-   [**\_поdesc заглушки MIDL \_**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_desc)
-   [**\_сообщение заглушки MIDL \_**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_message)
-   [**проксифилеинфо**](/windows/win32/api/rpcproxy/ns-rpcproxy-proxyfileinfo)
-   [**\_сообщение RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message)

 

 