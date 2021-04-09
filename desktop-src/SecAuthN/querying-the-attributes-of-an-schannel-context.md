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
# <a name="querying-the-attributes-of-an-schannel-context"></a>Запрос атрибутов контекста SChannel

Функция [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) предоставляет сведения о [*контексте безопасности*](../secgloss/s-gly.md), относящиеся к SChannel. Большая часть информации изначально указывается при создании контекста с помощью функции Client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) или Server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Некоторые сведения указываются при получении маркера для учетных данных, используемых для создания контекста. Дополнительные сведения см. в разделе [Получение учетных данных SChannel](obtaining-schannel-credentials.md).

 

 
