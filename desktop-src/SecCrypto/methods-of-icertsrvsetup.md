---
description: Следующие методы определяются интерфейсом Ицертсрвсетуп. Методы доступа к свойствам не показаны здесь. Сведения о свойствах Ицертсрвсетуп см. в разделе Свойства Ицертсрвсетуп.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Методы Ицертсрвсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28274e1f59a4c229587f7e9f73222381ca89cff1a112ef7dc633f7a0c32dd434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407894"
---
# <a name="methods-of-icertsrvsetup"></a>Методы Ицертсрвсетуп

Следующие методы определяются интерфейсом [**ицертсрвсетуп**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) . Методы доступа к свойствам не показаны здесь. Сведения о свойствах **ицертсрвсетуп** см. в разделе [Свойства ицертсрвсетуп](properties-of-icertsrvsetup.md).



| Метод                                                                         | Описание                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**каимпортпфкс**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Импортирует сертификат центра сертификации (ЦС) и связанный с ним закрытый ключ в хранилище LocalMachine.                                                                                                                                          |
| [**жеткасетуппроперти**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Возвращает значение свойства для конфигурации ЦС.                                                                                                                                                                                                             |
| [**жетексистингкацертификатес**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Возвращает коллекцию объектов **кцертсрвсетупкэйинформатион** , представляющих действительные сертификаты ЦС, установленные на компьютере в данный момент.                                                                                                                  |
| [**жесашалгорисмлист**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Возвращает список алгоритмов хэширования, поддерживаемых указанным [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для алгоритма подписи асимметричного ключа. |
| [**жеткэйленгслист**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Возвращает список длин ключей, поддерживаемых указанным CSP.                                                                                                                                                                                              |
| [**жетприватекэйконтаинерлист**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Возвращает список имен контейнеров ключей, сохраненных указанным CSP для алгоритмов асимметричного ключа подписи.                                                                                                                                                 |
| [**жетпровидернамелист**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Возвращает список CSP, которые предоставляют алгоритмы подписи асимметричных ключей на компьютере.                                                                                                                                                                   |
| [**жетсуппортедкатипес**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Возвращает типы центров сертификации, которые могут быть установлены на компьютере в контексте вызывающего объекта.                                                                                                                                                                       |
| [**инитиализедефаултс**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Инициализирует объект **кцертсрвсетуп** со значениями по умолчанию, чтобы разрешить установку роли ЦС.                                                                                                                                                           |
| [**Взнос**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Устанавливает роль CA, настроенную в объекте **кцертсрвсетуп** .                                                                                                                                                                                         |
| [**испропертедитабле**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Указывает вызывающему объекту, можно ли изменять указанное свойство.                                                                                                                                                                                       |
| [**Postuninstall выполняются**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | Не реализовано и зарезервировано для будущего использования.                                                                                                                                                                                                        |
| [**Команды сценария preuninstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Временно сохраняет сведения о состоянии для конкретной роли.                                                                                                                                                                                                        |
| [**сеткадистингуишеднаме**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Задает общее имя ЦС и необязательный суффикс различающегося имени.                                                                                                                                                                                          |
| [**сеткасетуппроперти**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Задает значение свойства для конфигурации ЦС.                                                                                                                                                                                                             |
| [**сетдатабасеинформатион**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Задает сведения, связанные с базой данных для роли ЦС.                                                                                                                                                                                                    |
| [**сетпаренткаинформатион**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Задает сведения о родительском ЦС для конфигурации подчиненного ЦС.                                                                                                                                                                                        |
| [**сетвебкаинформатион**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Задает сведения о ЦС для роли веб-регистрации ЦС.                                                                                                                                                                                                   |



 

 

 
