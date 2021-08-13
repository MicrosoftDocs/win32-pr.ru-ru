---
description: Предоставляет сведения о контексте безопасности, относящиеся к SChannel.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Запрос атрибутов контекста SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f00f6d5f0660bbb3a0d4ce5890ab415325707dbda4087d025a010efdb3fd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919943"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Запрос атрибутов контекста SChannel

Функция [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) предоставляет сведения о [*контексте безопасности*](../secgloss/s-gly.md), относящиеся к SChannel. Большая часть информации изначально указывается при создании контекста с помощью функции Client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) или Server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Некоторые сведения указываются при получении маркера для учетных данных, используемых для создания контекста. Дополнительные сведения см. в разделе [Получение учетных данных SChannel](obtaining-schannel-credentials.md).

 

 
