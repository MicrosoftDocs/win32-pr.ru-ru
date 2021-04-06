---
description: Функция AreFileApisANSI определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Определение кодовой страницы текущей кодировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910163"
---
# <a name="determining-the-current-character-set-code-page"></a>Определение кодовой страницы текущей кодировки

Функция [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM. Функция [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) заставляет функции использовать кодовую страницу ANSI. Функция [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) заставляет функции использовать кодовую страницу OEM.

По умолчанию функции файлового ввода-вывода используют имена файлов ANSI. Функции, экспортированные Kernel32.dll, которые принимают или возвращают имена файлов, затрагиваются параметром кодовой страницы файла.

И [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) , и [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) устанавливают кодовую страницу для каждого процесса, а не для каждого потока или для каждого компьютера.

 

 



