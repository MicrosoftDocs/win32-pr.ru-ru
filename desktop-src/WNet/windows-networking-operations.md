---
title: Сетевые операции Windows
description: Приложение может использовать функции Внет для просмотра, добавления или отмены сетевых подключений в любом месте иерархии сети.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337921"
---
# <a name="windows-networking-operations"></a>Сетевые операции Windows

Приложение может использовать функции Внет для просмотра, добавления или отмены сетевых подключений в любом месте иерархии сети.

*Постоянное подключение* — это сетевое подключение, которое система автоматически восстанавливает при входе пользователя в систему. Вы можете вызвать функции [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (или [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) и [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) , чтобы управлять тем, является ли сетевое подключение постоянным от одного сеанса к другому.

Чтобы найти имя пользователя по умолчанию или имя пользователя, используемое для установления сетевого подключения, вызовите функцию [**внетжетусер**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .

Помимо вызова функций Внет, процесс также может использовать маилслотс и именованные каналы для взаимодействия с другим процессом. Дополнительные сведения см. в разделе [маилслотс](/windows/desktop/ipc/mailslots) и [каналы](/windows/desktop/ipc/pipes).

 

 