---
description: Диспетчер транзакций ядра (KTM) — это служба управления транзакциями. Она делает транзакции доступными как объекты ядра и предоставляет службы управления транзакциями системным компонентам, таким как транзакционная NTFS (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: О программе KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081496"
---
# <a name="about-ktm"></a>О программе KTM

Диспетчер транзакций ядра (KTM) — это служба управления транзакциями. Она делает транзакции доступными как объекты ядра и предоставляет службы управления транзакциями системным компонентам, таким как [транзакционная NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).

В следующих разделах описываются варианты использования и функции KTM:

-   [Что такое транзакция?](what-is-a-transaction.md)
-   [Работа с транзакциями](programming-model.md)
-   [Запись диспетчер ресурсов](writing-a-resource-manager.md)
-   [Взаимодействие с другими функциями Windows](interoperability-with-other-windows-features.md)
-   [Права доступа и безопасности KTM](ktm-security-and-access-rights.md)

Для работы KTM используется [Файловая система CLFS](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) . CLFS — это система ведения журналов, которая может включать транзакции.

 

 
