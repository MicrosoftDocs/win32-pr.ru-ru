---
description: В следующих разделах описываются файлы символов и функции, предоставляемые функциями DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: О DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162702"
---
# <a name="about-dbghelp"></a>О DbgHelp

В следующих разделах описываются файлы символов и функции, предоставляемые [функциями DBGHELP](dbghelp-functions.md).

-   [Версии DbgHelp](dbghelp-versions.md)
-   [Файлы символов](symbol-files.md)
-   [Обработка символов](symbol-handling.md)
-   [Серверы символов и хранилища символов](symbol-servers-and-symbol-stores.md)
-   [Файлы минидампа](minidump-files.md)
-   [Исходный сервер](source-server-and-source-indexing.md)
-   [Поддержка платформы обновлена](updated-platform-support.md)

Обратите внимание, что все [функции DBGHELP](dbghelp-functions.md) являются отдельными потоками. Таким образом, вызовы из более чем одного потока в эту функцию, скорее всего, приведут к непредвиденному поведению или повреждению памяти. Чтобы избежать этого, необходимо синхронизировать все одновременные вызовы из более чем одного потока в эту функцию.

 

 



