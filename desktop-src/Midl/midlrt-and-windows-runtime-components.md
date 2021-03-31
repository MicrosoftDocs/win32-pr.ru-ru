---
title: Компоненты MIDLRT и среда выполнения Windows
description: Показывает, как создать файлы метаданных (WinMD), представляющие API для пользовательских компонентов среда выполнения Windows.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL компилятора MIDL
- MIDL компилятора MIDL, MIDL и среда выполнения Windows WinRT
- среда выполнения Windows MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533602"
---
# <a name="midlrt-and-windows-runtime-components"></a>Компоненты MIDLRT и среда выполнения Windows

Показывает, как создать файлы метаданных (WinMD), представляющие API для пользовательских компонентов среда выполнения Windows.


Используйте компилятор MIDLRT для создания файлов метаданных (WinMD) для пользовательских компонентов среда выполнения Windows.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Файлы МДМЕРЖЕ и Metadata](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




