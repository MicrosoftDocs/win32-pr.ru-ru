---
description: модуль записи xps-документов (майкрософт) (мксдв) — это драйвер, позволяющий Windowsному приложению создавать файлы документов xps в версиях Windows, начиная с Windows XP с пакетом обновления 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Модуль записи XPS-документов (Майкрософт) (МКСДВ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba69a6efff4f2da0ab0cc03bdc71468dada14c457de7685053096d2fba672d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938893"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Модуль записи XPS-документов (Майкрософт) (МКСДВ)

модуль записи xps-документов (майкрософт) (мксдв) — это драйвер, позволяющий Windowsному приложению создавать файлы документов xps в версиях Windows, начиная с Windows XP с пакетом обновления 2 (SP2). использование мксдв позволяет приложению Windows сохранять свое содержимое как документ XPS, не изменяя программный код приложения.

## <a name="when-to-use"></a>Назначение

как пользователь, вы выбрали мксдв, когда хотите создать документ XPS из Windows приложения, которое не поддерживает сохранение его содержимого в виде xps-документа.

Разработчикам приложений рекомендуется МКСДВ пользователям, желающим создавать XPS-документы, если приложение не предлагает возможность сохранения в виде документа XPS. Дополнительные сведения о спецификации документа XML и документах XPS см. в [статье Спецификация XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) и [Спецификация XPS и загрузка лицензий](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

мксдв устанавливается автоматически на Windows Vista и более поздних версиях Windows и может быть загружен и установлен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.

## <a name="installation"></a>Установка

в Windows Vista и более поздних версиях Windows мксдв устанавливается автоматически при установке операционной системы.

**Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003**: скачайте и установите платформу .net Framework 3,0 или необходимый пакет XPS из [центра загрузки майкрософт](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Использование

При установке МКСДВ отображается в виде доступной очереди печати в диалоговом окне Печать, представленном приложением. Если в качестве принтера выбран МКСДВ, пользователю будет предложено ввести имя файла для создания в качестве документа XPS, записывающего выходные данные для печати приложения.

на следующем рисунке показан мксдв, выбранный в качестве принтера в диалоговом окне "общие печать" Windows Vista.

![Изображение диалогового окна «Печать», в котором отображается выбор средства записи документов XPS (Microsoft) (мксдв)](images/choosingmxdwinvista.gif)

Разработчики приложений могут настраивать выходные данные МКСДВ с помощью [параметров конфигурации мксдв](mxdw-configuration-settings.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Спецификация XPS и загрузка лицензий](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Средство соответствия isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Параметры конфигурации МКСДВ](mxdw-configuration-settings.md)
</dt> </dl>

 

 
