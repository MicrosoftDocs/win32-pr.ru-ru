---
description: В следующих разделах описываются файлы символов и функции, предоставляемые функциями DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: О DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141150"
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

 

 



