---
description: 'Дополнительные сведения о: расширяемый Справочник по управляемому подсистеме хранилища'
title: Управляемый Справочник по расширенному подсистеме хранилища
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080444"
---
# <a name="extensible-storage-engine-managed-reference"></a>Управляемый Справочник по расширенному подсистеме хранилища

Найдите справочные сведения о библиотеке Манажедесент. Библиотека Манажедесент предоставляет управляемый доступ к ESENT, встраиваемому ядру СУБД, который является собственным для Windows.


_**Применимо к:** Windows | Windows Server_

**В этой статье:**  
Как библиотека Манажедесент отличается от ESENT?  
Требования  
Содержание раздела  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>Как библиотека Манажедесент отличается от ESENT?

ESENT — это внедряемое, транзакционное ядро СУБД, которое позволяет создавать пользовательские приложения, требующие надежного хранения данных с высокой производительностью и низкой нагрузкой. Подсистема ESENT может помочь в использовании данных в диапазоне от чего-нибудь простого, так же как в хэш таблице, которая слишком велика для хранения в памяти, на нечто более сложное, например в приложении с таблицами, столбцами и индексами. Чтобы создать приложение с помощью ESENT, используйте библиотеку DLL esent.dll, которая является частью операционной системы Windows, и напишите код с помощью C/C++. Дополнительные сведения о ESENT см. в [справочнике по расширенному подсистеме хранилища](./extensible-storage-engine-reference.md).

Манажедесент построен на esent.dll, который является частью Windows, поэтому дополнительные неуправляемые двоичные файлы для загрузки и установки отсутствуют. С помощью библиотеки Манажедесент можно создать приложение с помощью управляемого языка, например C, \# а не c/C++. Библиотека использует те же имена типов и членов для предоставления API ESE, поэтому, если вы уже знакомы со структурой этого API, вы можете легко перейти к этой управляемой библиотеке.

## <a name="requirements"></a>Требования

Для этой управляемой библиотеки требуется следующее:

  - Компьютер под управлением версии Windows, начиная с Windows Vista

  - Visual Studio 2012

  - Платформа .NET Framework версии 4.5

## <a name="in-this-section"></a>Содержание раздела

  - [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
