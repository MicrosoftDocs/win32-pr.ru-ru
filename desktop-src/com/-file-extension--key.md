---
title: Ключ file_extension
description: Связывает расширение имени файла с ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889147"
---
# <a name="file_extension-key"></a><\_> ключ расширения файла

Связывает расширение имени файла с ProgID.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Комментарии

Сведения, содержащиеся в ключе расширения имени файла, используются как в проводнике Windows, так и в моникерах файлов. [**Жетклассфиле**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) использует ключ расширения имени файла для предоставления связанного идентификатора CLSID.

Ключ **\_ \_ \\ \\ классов программного обеспечения файла hKey на локальном компьютере** соответствует **\_ \_ корневому ключу classes** , который был сохранен для совместимости с предыдущими версиями com.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**жетклассфиле**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




