---
description: После загрузки файла символов в обработчик символов приложение может использовать функции указателя символов для возврата символьной информации для указанного адреса.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Поиск символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f65830032cf363771b14f779726c59d976e8d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140786"
---
# <a name="finding-symbols"></a>Поиск символов

После загрузки файла символов в обработчик символов приложение может использовать функции указателя символов для возврата символьной информации для указанного адреса. Эти функции также могут найти имя файла исходного кода и расположение номера строки для адреса.

## <a name="enumerating-symbol-files"></a>Перечисление файлов символов

Чтобы получить список всех файлов символов, загруженных по имени модуля, вызовите функцию [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) . Пример см. в разделе [Перечисление модулей символов](enumerating-symbol-modules.md). Чтобы получить список символов для данного модуля, вызовите функцию [**сименумсимболс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) . Пример см. в разделе [перечисление символов](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Извлечение символов по адресу

Чтобы получить символьные сведения для определенного адреса, используйте функцию [**симфромаддр**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Эта функция получает сведения и сохраняет их в структуре [**\_ сведений о символах**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Так как имена символов имеют переменную длину, необходимо указать дополнительное место в буфере после объявления структуры **\_ сведений о символах** . Пример см. в разделе [Получение символьной информации по адресу](retrieving-symbol-information-by-address.md).

Обратите внимание, что адрес не обязательно должен находиться на границе символа. Если адрес поступает после начала символа, но перед концом символа (начало символа плюс размер символа), функция обнаружит символ.

## <a name="retrieving-symbols-by-symbol-name"></a>Извлечение символов по имени символа

Чтобы получить символьную информацию в [**структуре \_ символьной**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) информации для конкретного модуля и имени символа, используйте функцию [**симфромнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Если задана отложенная загрузка символов, **симфромнаме** будет пытаться загрузить файл символов для модуля, если он еще не загружен. Чтобы указать имя модуля вместе с именем символа, используйте *модуль* синтаксиса! *Симнаме*. Символ "!" отделяет имя модуля от имени символа. Пример см. в разделе [Получение символьной информации по имени](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Получение номеров строк по адресу

Чтобы получить расположение исходного кода для определенного адреса, используйте функцию [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) . Эта функция заполняет структуру [**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) , включающую в себя имя исходного файла и номер строки, на которую указывает указанный адрес. Пример см. в разделе [Получение символьной информации по адресу](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Извлечение номеров строк по имени символа

Чтобы получить расположение исходного кода для конкретного имени символа, используйте функцию [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) . Эта функция похожа на [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), но получает структуру [**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) . Чтобы использовать [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) или **SymGetLineFromName64**, необходимо задать параметр Load Lines ( \_ строки загрузки Симопт \_ ) с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Пример см. в разделе [Получение символьной информации по имени](retrieving-symbol-information-by-name.md).

 

 



