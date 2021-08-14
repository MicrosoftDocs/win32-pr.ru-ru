---
description: Диспетчер транзакций ядра (KTM) — это служба управления транзакциями. Она делает транзакции доступными как объекты ядра и предоставляет службы управления транзакциями системным компонентам, таким как транзакционная NTFS (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: О программе KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a08aca70afbd44b1c23243239ec86839639ff46c3e16e698b65e96ff8a250b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388923"
---
# <a name="about-ktm"></a>О программе KTM

Диспетчер транзакций ядра (KTM) — это служба управления транзакциями. Она делает транзакции доступными как объекты ядра и предоставляет службы управления транзакциями системным компонентам, таким как [транзакционная NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).

В следующих разделах описываются варианты использования и функции KTM:

-   [Что такое транзакция?](what-is-a-transaction.md)
-   [Работа с транзакциями](programming-model.md)
-   [Запись диспетчер ресурсов](writing-a-resource-manager.md)
-   [взаимодействие с другими функциями Windows](interoperability-with-other-windows-features.md)
-   [Права доступа и безопасности KTM](ktm-security-and-access-rights.md)

Для работы KTM используется [Файловая система CLFS](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) . CLFS — это система ведения журналов, которая может включать транзакции.

 

 
