---
description: Регистрация ошибок
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Регистрация ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7402ade284f0d9a71b032f233276277dfdcd8c5e2844c85f03782caed101d095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685154"
---
# <a name="logging-errors"></a>Регистрация ошибок

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

[службы DirectShow editing Services](directshow-editing-services.md) (DES) предоставляют встроенный механизм ведения журнала ошибок, возникающих при загрузке, построении или визуализации проекта DES. В этой статье представлен пример консольного приложения, которое загружает файл XML-проекта и пытается выполнить его визуализацию. При возникновении ошибки приложение выводит сообщение об ошибке в окне консоли. Пример кода, представленный в этой статье, основан на примере [загрузки и предварительного просмотра Project](loading-and-previewing-a-project.md).

> [!Note]  
> Приложению не требуется реализовывать ведение журнала ошибок. DES не регистрирует ошибки, если вы явно не запрашиваете его.

 

В этой статье предполагается, что вы знакомы с программированием клиента COM и моделью временной шкалы DES. Кроме того, необходимо ознакомиться с основами программирования объектов COM. Сведения о шкалах времени в DES см. [в разделе Модель временной шкалы](the-timeline-model.md).

Эта статья состоит из следующих разделов:

-   [Общие сведения о ведении журнала ошибок](overview-of-error-logging.md)
-   [Создание класса ведения журнала ошибок](creating-an-error-logging-class.md)
-   [Реализация Иамеррорлог](implementing-iamerrorlog.md)
-   [Настройка журнала ошибок](setting-the-error-log.md)
-   [Ведение журнала ошибок DES: пример кода](des-error-logging--example-code.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[использование служб DirectShow editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 



