---
title: аутоконвертто
description: Задает автоматическое преобразование данного класса объектов в новый класс объектов.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- COM раздела реестра Аутоконвертто
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887420"
---
# <a name="autoconvertto"></a><span data-ttu-id="a1019-104">аутоконвертто</span><span class="sxs-lookup"><span data-stu-id="a1019-104">AutoConvertTo</span></span>

<span data-ttu-id="a1019-105">Задает автоматическое преобразование данного класса объектов в новый класс объектов.</span><span class="sxs-lookup"><span data-stu-id="a1019-105">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a1019-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="a1019-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a><span data-ttu-id="a1019-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1019-107">Remarks</span></span>

<span data-ttu-id="a1019-108">Это значение **reg \_ SZ** , указывающее идентификатор класса объекта, в который необходимо преобразовать заданный объект или класс объектов.</span><span class="sxs-lookup"><span data-stu-id="a1019-108">This is a **REG\_SZ** value that specifies the class identifier of the object to which the given object or class of objects should be converted.</span></span>

<span data-ttu-id="a1019-109">Этот ключ обычно используется для автоматического преобразования файлов, созданных в более старой версии приложения, в более новую версию приложения.</span><span class="sxs-lookup"><span data-stu-id="a1019-109">This key is typically used to automatically convert files created by an older version of an application to a newer version of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1019-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a1019-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1019-111">**оледоаутоконверт**</span><span class="sxs-lookup"><span data-stu-id="a1019-111">**OleDoAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[<span data-ttu-id="a1019-112">**олежетаутоконверт**</span><span class="sxs-lookup"><span data-stu-id="a1019-112">**OleGetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[<span data-ttu-id="a1019-113">**олесетаутоконверт**</span><span class="sxs-lookup"><span data-stu-id="a1019-113">**OleSetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




