---
description: Функция AreFileApisANSI определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Определение кодовой страницы текущей кодировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150661"
---
# <a name="determining-the-current-character-set-code-page"></a>Определение кодовой страницы текущей кодировки

Функция [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM. Функция [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) заставляет функции использовать кодовую страницу ANSI. Функция [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) заставляет функции использовать кодовую страницу OEM.

По умолчанию функции файлового ввода-вывода используют имена файлов ANSI. Функции, экспортированные Kernel32.dll, которые принимают или возвращают имена файлов, затрагиваются параметром кодовой страницы файла.

И [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) , и [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) устанавливают кодовую страницу для каждого процесса, а не для каждого потока или для каждого компьютера.

 

 



