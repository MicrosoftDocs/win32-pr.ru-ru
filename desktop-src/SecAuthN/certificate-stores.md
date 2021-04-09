---
description: Сертификаты клиента и сервера должны храниться в хранилище сертификатов, доступном для процесса приложения.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Хранилища сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080541"
---
# <a name="certificate-stores"></a>Хранилища сертификатов

Сертификаты [*клиента*](/windows/desktop/SecGloss/c-gly) и [*сервера*](/windows/desktop/SecGloss/s-gly) должны храниться в [*хранилище сертификатов*](/windows/desktop/SecGloss/c-gly) , доступном для процесса приложения. Как правило, это хранилище My, также известное как личное хранилище. Клиентские приложения, такие как Internet Explorer, обычно используют мое хранилище текущего пользователя, а на таких серверах, как службы IIS (IIS), используется система My Store локального компьютера.

Корневое хранилище и хранилище [*центра сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) используются, когда канал Schannel или приложение создает цепочку сертификатов для отправки на удаленный компьютер. Эти хранилища используются для проверки полученной цепочки сертификатов. Дополнительные сведения см. в статье [выполнение проверки подлинности с помощью канала Schannel](performing-authentication-using-schannel.md).

 

 
