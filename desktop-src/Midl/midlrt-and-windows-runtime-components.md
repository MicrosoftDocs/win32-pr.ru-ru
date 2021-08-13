---
title: компоненты MIDLRT и среда выполнения Windows
description: показывает, как создать файлы метаданных (winmd), представляющие API для пользовательских компонентов среда выполнения Windows.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL компилятора MIDL
- midl компилятора midl, midl и среда выполнения Windows winrt
- Windows MIDL среды выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f827178216bbb7e78c16f2c11fa68b29b2eb50cfc0714a0ed53b02ce5bdc4ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642908"
---
# <a name="midlrt-and-windows-runtime-components"></a>компоненты MIDLRT и среда выполнения Windows

показывает, как создать файлы метаданных (winmd), представляющие API для пользовательских компонентов среда выполнения Windows.


используйте компилятор MIDLRT для создания файлов метаданных (winmd) для пользовательских компонентов среда выполнения Windows.

При создании файлов метаданных их можно составить в более эффективный пакет с помощью служебной программы МДМЕРЖЕ. Дополнительные сведения см. в разделе [мдмерже и файлы метаданных](mdmerge-and-metadata-files.md).


Использование MIDLRT аналогично использованию компилятора MIDL. Запустите MIDLRT из командной строки с помощью следующей команды:

**midlrt**  *<* **Параметры** _>_ **filename. idl**

Здесь **Параметры** * < * _>_ представляют параметры командной строки, которые необходимо использовать, а filename. IDL — имя IDL-файла для компиляции.


В следующем списке приведены параметры командной строки, которые MIDLRT.EXE использует.

<dl>

[**\_класс/енум**](-enum-class.md)  
[**/Метадата \_ dir**](-metadata-dir.md)  
[**/номидл**](-nomidl.md)  
[**/номд**](-nomd.md)  
[**\_префикс/НС**](-ns-prefix.md)  
[**/WinMD**](-winmd.md)  
[**/WinRT**](-winrt.md)  
</dl>

Полный список ключей и параметров компилятора MIDLRT доступен при использовании компилятора MIDLRT [**/Help**](-help-.md) и/? аргументы. Параметры упорядочены по категориям. Дополнительные сведения см. в [справочнике по языку MIDL Command-Line](midl-command-line-reference.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Файлы МДМЕРЖЕ и Metadata](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




