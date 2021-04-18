---
title: UI_PKEY_TooltipTitle
description: Определяет свойство UI \_ PKEY \_ тултиптитле.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700635"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="df4ae-103">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="df4ae-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="df4ae-104">Определяет свойство UI \_ PKEY \_ тултиптитле.</span><span class="sxs-lookup"><span data-stu-id="df4ae-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="df4ae-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df4ae-105">Remarks</span></span>

<span data-ttu-id="df4ae-106">UI \_ PKEY \_ тултиптитле используется приложением для запроса подсказки вкладок, групп, кнопок, элементов коллекции и других элементов управления ленты.</span><span class="sxs-lookup"><span data-stu-id="df4ae-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="df4ae-107">Значение свойства — это строка, ограниченная любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="df4ae-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="df4ae-108">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="df4ae-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="df4ae-109">Выравнивание по правому краю не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="df4ae-109">Right alignment is not supported.</span></span>

<span data-ttu-id="df4ae-110">Максимальная длина пользовательского интерфейса \_ PKEY \_ тултиптитле не ограничена.</span><span class="sxs-lookup"><span data-stu-id="df4ae-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="df4ae-111">Чтобы отобразить амперсанд во всплывающей подсказке, необходимо экранировать Специальный символ с двойным амперсандом ( `&&` ), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="df4ae-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="df4ae-112">См. также</span><span class="sxs-lookup"><span data-stu-id="df4ae-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df4ae-113">Свойства ресурса</span><span class="sxs-lookup"><span data-stu-id="df4ae-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="df4ae-114">**Command. Тултиптитле**</span><span class="sxs-lookup"><span data-stu-id="df4ae-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="df4ae-115">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="df4ae-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




