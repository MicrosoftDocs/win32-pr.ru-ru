---
description: На томе файловой системы NTFS каждый файл и каталог имеет атрибут сжатия.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Атрибут Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913711"
---
# <a name="compression-attribute"></a>Атрибут Compression

На томе файловой системы NTFS каждый файл и каталог имеет *атрибут сжатия*. Другие файловые системы также могут реализовывать атрибут сжатия для отдельных файлов и каталогов.

Определить, поддерживает ли файловая система атрибут сжатия для файлов и каталогов, можно путем вызова функции [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и проверки флага бита **\_ \_ сжатия** файлового файла.

Используйте функцию [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) или [**сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) , чтобы определить атрибут сжатия файла или каталога.

Если задан атрибут сжатия файла (**\_ \_ сжатый атрибут файла**), все данные в файле сжимаются. Если атрибут является четким, ни один из данных в файле не сжимается. Нет частично сжатого состояния с точки зрения программирования в пользовательском режиме; атрибут Compression является простым логическим индикатором состояния сжатия.

Атрибут сжатия каталога предоставляет атрибут сжатия по умолчанию для вновь создаваемых файлов и подкаталогов. При вызове [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) или [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) для создания нового файла или каталога новый файл или каталог наследует атрибут сжатия своего родительского каталога.

Чтобы изменить **\_ \_ сжатый атрибут файла** для файла или каталога, необходимо использовать функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с управляющим кодом [**фсктл \_ Set \_ Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Константы атрибутов файлов**](file-attribute-constants.md)
</dt> </dl>

 

 
