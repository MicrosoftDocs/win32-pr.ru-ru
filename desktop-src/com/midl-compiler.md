---
title: Компилятор MIDL
description: Компилятор MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa57131e31e9c6273270a771f9ba862d73bc142
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794125"
---
# <a name="midl-compiler"></a>Компилятор MIDL

Компилятор MIDL обрабатывает IDL-файл для создания библиотеки типов и выходных файлов. Тип выходных файлов, создаваемых компилятором MIDL, зависит от атрибутов, указанных в списке атрибутов интерфейса IDL-файла.

Если список атрибутов содержит \[ [](/windows/desktop/Midl/object) \] ключевое слово Object, компилятор MIDL создает выходные файлы интерфейса COM: файл прокси интерфейса, файл заголовка интерфейса и файл глобального уникального идентификатора (GUID) для интерфейса. Если IDL-файл содержит оператор [**Library**](/windows/desktop/Midl/library) , MIDL создает файл библиотеки типов с расширением TLB. Если в IDL-файле есть интерфейсы, не имеющие \[  \] ключевого слова Object и не заключенные в оператор **Library** , компилятор MIDL создает выходные файлы интерфейса, подходящие для удаленных вызовов процедур (RPC): файл заглушки клиента, файл заглушки сервера и файл заголовка. Дополнительные сведения см. в разделах [определения интерфейса и библиотеки типов](/windows/desktop/Midl/interface-definitions-and-type-libraries) и [Создание библиотеки типов с помощью MIDL](/windows/desktop/Midl/generating-a-type-library-with-midl-2).

Создание библиотеки типов и выходных файлов из IDL-файла:

-   В командной строке выполните команду.

     *имя файла* MIDL

    где *filename* — имя IDL-файла.

Компилятор MIDL также поддерживает несколько необязательных параметров. Полный список см. в разделе "Справочник по MIDL Command-Line" в документации по Visual C++ или выполните следующую командную строку:

**MIDL/?**

## <a name="related-topics"></a>См. также

<dl> <dt>

[язык MIDL](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Преобразование в C++](translating-to-c--.md)
</dt> </dl>

 

 