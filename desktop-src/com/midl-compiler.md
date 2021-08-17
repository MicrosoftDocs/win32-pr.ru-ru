---
title: Компилятор MIDL
description: Компилятор MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db4afbbe8c7a82f4335855b40e578fe2eea046fa4c7f0560e3e297b559a67ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736433"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[язык MIDL](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Преобразование в C++](translating-to-c--.md)
</dt> </dl>

 

 