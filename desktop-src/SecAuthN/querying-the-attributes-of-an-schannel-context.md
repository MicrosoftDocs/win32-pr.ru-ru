---
description: Предоставляет сведения о контексте безопасности, относящиеся к SChannel.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Запрос атрибутов контекста SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143702"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a><span data-ttu-id="4902f-103">Запрос атрибутов контекста SChannel</span><span class="sxs-lookup"><span data-stu-id="4902f-103">Querying the Attributes of an Schannel Context</span></span>

<span data-ttu-id="4902f-104">Функция [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) предоставляет сведения о [*контексте безопасности*](../secgloss/s-gly.md), относящиеся к SChannel.</span><span class="sxs-lookup"><span data-stu-id="4902f-104">The [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) function provides Schannel-specific information about a [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="4902f-105">Большая часть информации изначально указывается при создании контекста с помощью функции Client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) или Server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="4902f-105">Most of the information is originally specified when the context is created by using the client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) or server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="4902f-106">Некоторые сведения указываются при получении маркера для учетных данных, используемых для создания контекста.</span><span class="sxs-lookup"><span data-stu-id="4902f-106">Some information is specified when obtaining a handle to the credential used to create the context.</span></span> <span data-ttu-id="4902f-107">Дополнительные сведения см. в разделе [Получение учетных данных SChannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="4902f-107">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
