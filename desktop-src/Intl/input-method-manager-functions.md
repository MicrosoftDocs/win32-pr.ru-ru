---
description: В этом разделе описываются функции IMM.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Функции диспетчера методов ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c0f03c2e6d29b262bd97729b92f9eea5fbf99d09f52ea3fe2b3579646a6fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948739"
---
# <a name="input-method-manager-functions"></a>Функции диспетчера методов ввода

В этом разделе описываются функции IMM.



| Функция                                                           | Описание                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**креатеифекоммонинстанце**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Возвращает указатель на интерфейс [**ифекоммон**](/windows/desktop/api/Msime/nn-msime-ifecommon) .                                                          |
| [**креатеифедиктионаринстанце**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Возвращает указатель на интерфейс [**ифедиктионари**](/windows/desktop/api/Msime/nn-msime-ifedictionary) .                                                  |
| [**креатеифелангуажеинстанце**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Возвращает указатель на интерфейс [**ифелангуаже**](/windows/desktop/api/Msime/nn-msime-ifelanguage) .                                                      |
| [**енуминпутконтекст**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Определяемая приложением функция обратного вызова, обрабатывающая контексты ввода, предоставляемые функцией **имменуминпутконтекст** .   |
| [**енумрегистервордпрок**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Определяемая приложением функция обратного вызова, используемая с функцией **имменумрегистерворд** .                                   |
| [**иммассоЦиатеконтекст**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Связывает указанный входной контекст с указанным окном.                                                          |
| [**иммассоЦиатеконтекстекс**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Изменяет связь между контекстом метода ввода и указанным окном или его дочерними элементами.                         |
| [**иммконфигуреиме**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Отображает диалоговое окно Конфигурация для IME указанного идентификатора языка ввода.                                |
| [**иммкреатеконтекст**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Создает новый контекст ввода, выделяя память для контекста и инициализируя ее.                                        |
| [**иммдестройконтекст**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Освобождает входной контекст и освобождает связанную память.                                                                    |
| [**иммдисаблеиме**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Отключает редактор IME для потока или для всех потоков в процессе.                                                             |
| [**иммдисаблелегацииме**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | указывает, что этот поток является потоком пользовательского интерфейса приложения для хранилища Windows.                                                               |
| [**иммдисаблетекстфрамесервице**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | Не рекомендуется. Отключает службу текстового ввода для указанного потока.                                                            |
| [**имменуминпутконтекст**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Извлекает контекст ввода для указанного потока.                                                                      |
| [**имменумрегистерворд**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Перечисляет строки регистра, имеющие указанную строку чтения, стиль и строку регистра.                           |
| [**иммескапе**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Обращается к возможностям определенных редакторов IME, которые недоступны через другие функции API IME.                           |
| [**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Извлекает список кандидатов.                                                                                                |
| [**иммжеткандидателисткаунт**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Возвращает размер списков кандидатов.                                                                                 |
| [**иммжеткандидатевиндов**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Извлекает сведения о окне кандидатов.                                                                         |
| [**иммжеткомпоситионфонт**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Извлекает сведения о логическом шрифте, который в настоящее время используется для вывода символов в окне композиции.               |
| [**иммжеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Извлекает сведения о строке построения.                                                                        |
| [**иммжеткомпоситионвиндов**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Извлекает сведения о окне композиции.                                                                        |
| [**иммжетконтекст**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Извлекает контекст ввода, связанный с указанным окном.                                                          |
| [**иммжетконверсионлист**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Извлекает список результатов преобразования символов или слов без создания сообщений, связанных с IME.                   |
| [**иммжетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Извлекает текущее состояние преобразования.                                                                                   |
| [**иммжетдефаултимевнд**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Извлекает Стандартный маркер окна для класса IME.                                                                      |
| [**иммжетдескриптион**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Копирует Описание редактора IME в указанный буфер.                                                                 |
| [**иммжетгуиделине**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Извлекает сведения об ошибках.                                                                                        |
| [**иммжетимефиленаме**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Возвращает имя файла IME, связанного с заданным языковым стандартом ввода.                                             |
| [**иммжетимеменуитемс**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Извлекает пункты меню, зарегистрированные в меню IME указанного входного контекста.                                 |
| [**иммжетопенстатус**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Определяет, является ли редактор IME открытым или закрытым.                                                                              |
| [**иммжетпроперти**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Извлекает свойство и возможности IME, связанного с заданным языковым стандартом ввода.                             |
| [**иммжетрегистервордстиле**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Извлекает список стилей, поддерживаемых редактором IME, связанным с заданным языковым стандартом ввода.                            |
| [**иммжетстатусвиндовпос**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Извлекает расположение окна состояния.                                                                               |
| [**иммжетвиртуалкэй**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Извлекает исходное значение виртуального ключа, связанное с сообщением ввода ключа, которое уже обработано редактором IME.           |
| [**имминсталлиме**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Устанавливает редактор IME.                                                                                                           |
| [**иммисиме**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Определяет, имеет ли указанный язык ввода IME.                                                                       |
| [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Проверяет наличие сообщений, предназначенных для окна IME, и отправляет эти сообщения в указанное окно.                          |
| [**иммнотифиме**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Уведомляет IME об изменениях состояния входного контекста.                                                         |
| [**иммрегистерворд**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Регистрирует строку с словарем IME, связанным с заданным языковым стандартом ввода.                              |
| [**иммрелеасеконтекст**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Освобождает входной контекст и разблокирует память, связанную со входным контекстом.                                         |
| [**иммрекуестмессаже**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Запрашивает сообщение от приложения.                                                                                   |
| [**иммсеткандидатевиндов**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Задает сведения о окне кандидатов.                                                                              |
| [**иммсеткомпоситионфонт**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Задает логический шрифт, используемый для вывода символов в окне композиции.                                              |
| [**иммсеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Задает символы, атрибуты и предложения строк композиции и чтения.                                       |
| [**иммсеткомпоситионвиндов**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Задает расположение окна композиции.                                                                               |
| [**иммсетконверсионстатус**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Задает текущее состояние преобразования.                                                                                        |
| [**иммсетопенстатус**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Открывает или закрывает редактор IME.                                                                                                   |
| [**иммсетстатусвиндовпос**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Задает расположение окна состояния.                                                                                    |
| [**иммсимулатехоткэй**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Имитирует указанную горячую клавишу IME, что приводит к тому же ответу, что и при нажатии пользователем сочетания клавиш в указанном окне. |
| [**иммунрегистерворд**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Удаляет строку регистра из словаря IME, связанного с заданным языковым стандартом ввода.                       |



 

 

 



