---
title: Преобразование
description: Используется диалоговым окном преобразование для определения форматов, которые приложение может читать и записывать.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Преобразование ключа реестра COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532456"
---
# <a name="conversion"></a><span data-ttu-id="97b7d-104">Преобразование</span><span class="sxs-lookup"><span data-stu-id="97b7d-104">Conversion</span></span>

<span data-ttu-id="97b7d-105">Используется диалоговым окном **Преобразование** для определения форматов, которые приложение может читать и записывать.</span><span class="sxs-lookup"><span data-stu-id="97b7d-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="97b7d-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="97b7d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="97b7d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97b7d-107">Remarks</span></span>

<span data-ttu-id="97b7d-108">Сведения о преобразовании используются в диалоговом окне **Преобразование** для определения форматов, которые приложение может читать и записывать.</span><span class="sxs-lookup"><span data-stu-id="97b7d-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="97b7d-109">Формат файла с разделителями-запятыми обозначается числом, если он является одним из форматов буфера обмена, определенных в Windows. h.</span><span class="sxs-lookup"><span data-stu-id="97b7d-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="97b7d-110">Строка указывает, что формат не определен в Windows. h (частный).</span><span class="sxs-lookup"><span data-stu-id="97b7d-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="97b7d-111">В этом случае доступным для чтения и записываемым форматом является \_ Структура CF (частная).</span><span class="sxs-lookup"><span data-stu-id="97b7d-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="97b7d-112">Значение *рформат* указывает формат файла, который приложение может читать (преобразовать из).</span><span class="sxs-lookup"><span data-stu-id="97b7d-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="97b7d-113">Значение *рвформат* указывает формат файла, который приложение может читать и записывать (активировать как).</span><span class="sxs-lookup"><span data-stu-id="97b7d-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




