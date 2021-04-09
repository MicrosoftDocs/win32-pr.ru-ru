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
# <a name="file_extension-key"></a><span data-ttu-id="00e5a-103"><\_> ключ расширения файла</span><span class="sxs-lookup"><span data-stu-id="00e5a-103"><file\_extension> Key</span></span>

<span data-ttu-id="00e5a-104">Связывает расширение имени файла с ProgID.</span><span class="sxs-lookup"><span data-stu-id="00e5a-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="00e5a-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="00e5a-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="00e5a-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00e5a-106">Remarks</span></span>

<span data-ttu-id="00e5a-107">Сведения, содержащиеся в ключе расширения имени файла, используются как в проводнике Windows, так и в моникерах файлов.</span><span class="sxs-lookup"><span data-stu-id="00e5a-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="00e5a-108">[**Жетклассфиле**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) использует ключ расширения имени файла для предоставления связанного идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="00e5a-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="00e5a-109">Ключ **\_ \_ \\ \\ классов программного обеспечения файла hKey на локальном компьютере** соответствует **\_ \_ корневому ключу classes** , который был сохранен для совместимости с предыдущими версиями com.</span><span class="sxs-lookup"><span data-stu-id="00e5a-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00e5a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="00e5a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e5a-111">**FileType**</span><span class="sxs-lookup"><span data-stu-id="00e5a-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="00e5a-112">**жетклассфиле**</span><span class="sxs-lookup"><span data-stu-id="00e5a-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




