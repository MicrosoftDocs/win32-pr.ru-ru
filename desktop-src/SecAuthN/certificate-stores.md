---
description: Сертификаты клиента и сервера должны храниться в хранилище сертификатов, доступном для процесса приложения.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Хранилища сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64451ea7f568bb5e86289d5d9f1587d98b65aa1d53c14a4a251a5e61fe72b21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883494"
---
# <a name="certificate-stores"></a>Хранилища сертификатов

Сертификаты [*клиента*](/windows/desktop/SecGloss/c-gly) и [*сервера*](/windows/desktop/SecGloss/s-gly) должны храниться в [*хранилище сертификатов*](/windows/desktop/SecGloss/c-gly) , доступном для процесса приложения. Как правило, это хранилище My, также известное как личное хранилище. клиентские приложения, такие как Internet Explorer, обычно используют мое хранилище текущего пользователя, а на таких серверах, как службы IIS (IIS), используется система my store локального компьютера.

Корневое хранилище и хранилище [*центра сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) используются, когда канал Schannel или приложение создает цепочку сертификатов для отправки на удаленный компьютер. Эти хранилища используются для проверки полученной цепочки сертификатов. Дополнительные сведения см. в статье [выполнение проверки подлинности с помощью канала Schannel](performing-authentication-using-schannel.md).

 

 
