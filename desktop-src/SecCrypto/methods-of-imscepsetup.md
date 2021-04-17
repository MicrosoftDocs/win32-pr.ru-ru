---
description: Методы, определяемые интерфейсом Имсцепсетуп.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Методы Имсцепсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542335"
---
# <a name="methods-of-imscepsetup"></a>Методы Имсцепсетуп

Следующие методы определяются интерфейсом [**имсцепсетуп**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) . Методы доступа к свойствам не показаны здесь. Сведения о свойствах **имсцепсетуп** см. в разделе [Свойства имсцепсетуп](properties-of-imscepsetup.md).



| Метод                                                             | Описание                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жеткэйленгслист**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Возвращает список [*длин ключей*](../secgloss/k-gly.md) , поддерживаемых указанным [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP). |
| [**жетмсцепсетуппроперти**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Возвращает значение свойства для конфигурации службы регистрации сертификатов для сетевых устройств (NDES).                                                                                                                                                                                               |
| [**жетпровидернамелист**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Возвращает список поставщиков служб шифрования, которые предоставляют подписи асимметричных ключей и алгоритмы обмена на компьютере.                                                                                                                                                                              |
| [**инитиализедефаултс**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Инициализирует объект **кмсцепсетуп** со значениями по умолчанию, чтобы разрешить установку роли NDES.                                                                                                                                                                                  |
| [**Установка**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Устанавливает роль, настроенную в объекте **кмсцепсетуп** .                                                                                                                                                                                                                      |
| [**исмсцепсторимпти**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Всегда возвращает значение **типа Variant \_ true** и не должно использоваться.                                                                                                                                                                                                                          |
| [**Postuninstall выполняются**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Этот метод не реализован. Она зарезервирована для последующего использования.                                                                                                                                                                                                                    |
| [**Команды сценария preuninstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Удаляет параметры реестра и IIS для роли NDES.                                                                                                                                                                                                                              |
| [**сетаккаунтинформатион**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Задает сведения об учетной записи пользователя, используемые расширением службы NDES IIS для выполнения регистрации от имени сетевых устройств.                                                                                                                                                              |
| [**сетмсцепсетуппроперти**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Задает значение свойства для конфигурации NDES.                                                                                                                                                                                                                                  |



 

 

 
