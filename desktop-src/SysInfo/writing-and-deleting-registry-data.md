---
description: Приложение может использовать функцию RegSetValueEx для связывания значения и его данных с ключом. Список типов значений, поддерживаемых RegSetValueEx, см. в разделе Типы значений реестра.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Запись и удаление данных реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd4e80dc3320d1af0931e111c82f473e0edf56ac071443397ffc3da0918f7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883996"
---
# <a name="writing-and-deleting-registry-data"></a>Запись и удаление данных реестра

Приложение может использовать функцию [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) для связывания значения и его данных с ключом. Список типов значений, поддерживаемых **RegSetValueEx**, см. в разделе [типы значений реестра](registry-value-types.md).

Чтобы удалить значение из ключа, приложение может использовать функцию [**регделетевалуе**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) . Чтобы удалить ключ, можно использовать функцию [**регделетекэй**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) . Удаленный ключ не удаляется до тех пор, пока последний его маркер не будет закрыт. Подразделы и значения не могут быть созданы в удаленном ключе.

Невозможно заблокировать раздел реестра во время операции записи для синхронизации доступа к данным. Тем не менее можно управлять доступом к разделу реестра с помощью атрибутов безопасности. Дополнительные сведения см. в разделе [раздел реестра Security and Access Rights](registry-key-security-and-access-rights.md).

В одной транзакции может быть выполнено более одной операции с реестром. Чтобы связать раздел реестра с транзакцией, приложение может использовать функцию [**регкреатекэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) или [**регопенкэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) . Дополнительные сведения о транзакциях см. в разделе [Диспетчер транзакций ядра](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
