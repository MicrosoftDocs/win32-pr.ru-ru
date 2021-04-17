---
description: Привилегия указывает, владеет ли приложение или отслеживает сеанс.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684049"
---
# <a name="privilege"></a>Privilege

Привилегия указывает, владеет ли приложение или отслеживает сеанс. Если приложение владеет сеансом, ему разрешается выполнять различные операции с сеансами. Если приложение наблюдает только, оно получит сообщения о состоянии и сможет получить доступ к сведениям о сеансе, но любая попытка выполнить большинство операций приведет к ошибке.

Во время инициализации приложение сообщает TAPI, какой уровень привилегий требуется для этих адресов. TAPI предоставляет входящие сеансы только для приложений, зарегистрированных для владельца или владельца и прав монитора.

Права приложения в создаваемом сеансе всегда являются владельцами.

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллстатус**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **Двкаллпривилеже** , элемент [**линекаллстатус**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**линесеткаллпривилеже**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ привилегия**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), который вызывается с помощью элемента **CIL \_ нумберофовнерс** или **CIL \_ нумберофмониторс** [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
