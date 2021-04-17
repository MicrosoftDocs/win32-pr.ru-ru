---
description: Модуль записи XPS-документов (Майкрософт) (МКСДВ) — это драйвер, который позволяет приложению Windows создавать файлы документов XPS в версиях Windows, начиная с Windows XP с пакетом обновления 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Модуль записи XPS-документов (Майкрософт) (МКСДВ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693597"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Модуль записи XPS-документов (Майкрософт) (МКСДВ)

Модуль записи XPS-документов (Майкрософт) (МКСДВ) — это драйвер, который позволяет приложению Windows создавать файлы документов XPS в версиях Windows, начиная с Windows XP с пакетом обновления 2 (SP2). Использование МКСДВ позволяет приложению Windows сохранять содержимое как документ XPS, не изменяя программный код приложения.

## <a name="when-to-use"></a>Назначение

Как пользователь, вы выбрали МКСДВ, когда хотите создать документ XPS из приложения Windows, которое не поддерживает сохранение его содержимого в виде XPS-документа.

Разработчикам приложений рекомендуется МКСДВ пользователям, желающим создавать XPS-документы, если приложение не предлагает возможность сохранения в виде документа XPS. Дополнительные сведения о спецификации документа XML и документах XPS см. в [статье Спецификация XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) и [Спецификация XPS и загрузка лицензий](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

МКСДВ устанавливается автоматически в Windows Vista и более поздних версиях Windows и может быть загружен и установлен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.

## <a name="installation"></a>Установка

В Windows Vista и более поздних версиях Windows МКСДВ устанавливается автоматически при установке операционной системы.

**Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003**: Скачайте и установите .net Framework 3,0 или необходимый пакет XPS из [центра загрузки Майкрософт](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Использование

При установке МКСДВ отображается в виде доступной очереди печати в диалоговом окне Печать, представленном приложением. Если в качестве принтера выбран МКСДВ, пользователю будет предложено ввести имя файла для создания в качестве документа XPS, записывающего выходные данные для печати приложения.

На следующем рисунке показан МКСДВ, выбранный в качестве принтера в диалоговом окне Windows Vista Common Print.

![Изображение диалогового окна «Печать», в котором отображается выбор средства записи документов XPS (Microsoft) (мксдв)](images/choosingmxdwinvista.gif)

Разработчики приложений могут настраивать выходные данные МКСДВ с помощью [параметров конфигурации мксдв](mxdw-configuration-settings.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Спецификация XPS и загрузка лицензий](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Средство соответствия isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Параметры конфигурации МКСДВ](mxdw-configuration-settings.md)
</dt> </dl>

 

 
