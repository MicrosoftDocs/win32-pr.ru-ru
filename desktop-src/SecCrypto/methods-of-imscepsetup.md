---
description: Методы, определяемые интерфейсом Имсцепсетуп.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Методы Имсцепсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7dcadeb6c3815a37f1b1e87453a7ff737c70f53d76e0904bc67211ed7028f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622234"
---
# <a name="methods-of-imscepsetup"></a>Методы Имсцепсетуп

Следующие методы определяются интерфейсом [**имсцепсетуп**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) . Методы доступа к свойствам не показаны здесь. Сведения о свойствах **имсцепсетуп** см. в разделе [Свойства имсцепсетуп](properties-of-imscepsetup.md).



| Метод                                                             | Описание                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жеткэйленгслист**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Возвращает список [*длин ключей*](../secgloss/k-gly.md) , поддерживаемых указанным [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP). |
| [**жетмсцепсетуппроперти**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Возвращает значение свойства для конфигурации службы регистрации сертификатов для сетевых устройств (NDES).                                                                                                                                                                                               |
| [**жетпровидернамелист**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Возвращает список поставщиков служб шифрования, которые предоставляют подписи асимметричных ключей и алгоритмы обмена на компьютере.                                                                                                                                                                              |
| [**инитиализедефаултс**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Инициализирует объект **кмсцепсетуп** со значениями по умолчанию, чтобы разрешить установку роли NDES.                                                                                                                                                                                  |
| [**Взнос**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Устанавливает роль, настроенную в объекте **кмсцепсетуп** .                                                                                                                                                                                                                      |
| [**исмсцепсторимпти**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Всегда возвращает значение **типа Variant \_ true** и не должно использоваться.                                                                                                                                                                                                                          |
| [**Postuninstall выполняются**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Этот метод не реализован. Она зарезервирована для последующего использования.                                                                                                                                                                                                                    |
| [**Команды сценария preuninstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Удаляет параметры реестра и IIS для роли NDES.                                                                                                                                                                                                                              |
| [**сетаккаунтинформатион**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Задает сведения об учетной записи пользователя, используемые расширением службы NDES IIS для выполнения регистрации от имени сетевых устройств.                                                                                                                                                              |
| [**сетмсцепсетуппроперти**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Задает значение свойства для конфигурации NDES.                                                                                                                                                                                                                                  |



 

 

 
