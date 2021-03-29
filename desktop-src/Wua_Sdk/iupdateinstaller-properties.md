---
description: Интерфейс Иупдатеинсталлер определяет следующие свойства.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Свойства Иупдатеинсталлер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897562"
---
# <a name="iupdateinstaller-properties"></a>Свойства Иупдатеинсталлер

Интерфейс [**иупдатеинсталлер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) определяет следующие свойства.



| Свойство                                                                                      | Описание                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**алловсаурцепромптс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Возвращает и задает логическое значение, указывающее, следует ли отображать запросы к источнику пользователю при установке обновлений.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Возвращает и задает текущее клиентское приложение.                                                                                         |
| [**IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Возвращает логическое значение, указывающее, выполняется ли установка или удаление на компьютере в определенное время.        |
| [**Принудительно**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Возвращает или задает логическое значение, указывающее, следует ли принудительно установить или удалить обновление.                                       |
| [**паренсвнд**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Возвращает и задает маркер родительского окна, которое может содержать диалоговое окно.                                                            |
| [**парентвиндов**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Возвращает и задает интерфейс, представляющий родительское окно, которое может содержать диалоговое окно.                                          |
| [**ребутрекуиредбефореинсталлатион**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Возвращает логическое значение, указывающее, требуется ли перезагрузка системы перед установкой или удалением обновлений.                   |
| [**Обновления**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Возвращает и задает интерфейс, который содержит доступную только для чтения коллекцию обновлений, указанных для установки или удаления. |



 

 

 



