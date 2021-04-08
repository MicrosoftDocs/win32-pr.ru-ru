---
title: UI_PKEY_LabelDescription
description: Определяет свойство UI \_ PKEY \_ лабелдескриптион.
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888651"
---
# <a name="ui_pkey_labeldescription"></a><span data-ttu-id="9d875-103">UI \_ PKEY \_ лабелдескриптион</span><span class="sxs-lookup"><span data-stu-id="9d875-103">UI\_PKEY\_LabelDescription</span></span>

<span data-ttu-id="9d875-104">Определяет свойство UI \_ PKEY \_ лабелдескриптион.</span><span class="sxs-lookup"><span data-stu-id="9d875-104">Identifies the UI\_PKEY\_LabelDescription property.</span></span>

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="9d875-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d875-105">Remarks</span></span>

<span data-ttu-id="9d875-106">UI \_ PKEY \_ лабелдескриптион используется приложением для запроса описания, связанного с [ \_ \_ меткой PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="9d875-106">UI\_PKEY\_LabelDescription is used by an application to query the description associated with a [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span>

<span data-ttu-id="9d875-107">Значение свойства — это строка, ограниченная любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="9d875-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="9d875-108">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="9d875-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="9d875-109">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="9d875-109">The maximum length is unbounded.</span></span>

<span data-ttu-id="9d875-110">Выравнивание по правому краю не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d875-110">Right alignment is not supported.</span></span>

<span data-ttu-id="9d875-111">На следующем снимке экрана показано использование метки и связанного описания метки в меню приложения.</span><span class="sxs-lookup"><span data-stu-id="9d875-111">The following screen shot illustrates the use of a label and an associated label description in an Application Menu.</span></span>

![снимок экрана, отображающий метку и связанное с ним описание метки в меню приложения.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a><span data-ttu-id="9d875-113">См. также</span><span class="sxs-lookup"><span data-stu-id="9d875-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d875-114">Свойства ресурса</span><span class="sxs-lookup"><span data-stu-id="9d875-114">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="9d875-115">**Command. Лабелдескриптион**</span><span class="sxs-lookup"><span data-stu-id="9d875-115">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[<span data-ttu-id="9d875-116">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="9d875-116">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




