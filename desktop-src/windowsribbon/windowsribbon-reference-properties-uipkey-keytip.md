---
title: UI_PKEY_Keytip
description: Определяет свойство UI \_ PKEY \_ keytip.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986543"
---
# <a name="ui_pkey_keytip"></a><span data-ttu-id="fa83d-103">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="fa83d-103">UI\_PKEY\_Keytip</span></span>

<span data-ttu-id="fa83d-104">Определяет свойство UI \_ PKEY \_ keytip.</span><span class="sxs-lookup"><span data-stu-id="fa83d-104">Identifies the UI\_PKEY\_Keytip property.</span></span>

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="fa83d-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa83d-105">Remarks</span></span>

<span data-ttu-id="fa83d-106">UI \_ PKEY \_ KeyTip используется приложением для запроса сочетания клавиш для элемента управления ленты.</span><span class="sxs-lookup"><span data-stu-id="fa83d-106">UI\_PKEY\_Keytip is used by an application to query the keyboard accelerator of a ribbon control.</span></span>

<span data-ttu-id="fa83d-107">Это значение свойства является строкой, состоящей из любой последовательности символов, включая пробелы.</span><span class="sxs-lookup"><span data-stu-id="fa83d-107">This property value is a string, composed of any sequence of characters including white space.</span></span>

<span data-ttu-id="fa83d-108">Значение UI \_ PKEY \_ KeyTip выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню.</span><span class="sxs-lookup"><span data-stu-id="fa83d-108">The value of UI\_PKEY\_Keytip acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="fa83d-109">В этом случае платформа игнорирует \_ \_ значение KeyTip UI PKEY и вместо этого использует символ, предшествующий амперсанду, как указано в [ \_ \_ метке](windowsribbon-reference-properties-uipkey-label.md) [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или UI PKEY.</span><span class="sxs-lookup"><span data-stu-id="fa83d-109">In this case, the framework ignores the UI\_PKEY\_Keytip value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="fa83d-110">Если амперсанд не указан с помощью **команды Command. лабелтитле** или \_ метки PKEY пользовательского интерфейса \_ , то KeyTip или сочетания клавиш не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="fa83d-110">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="fa83d-111">Максимальная длина пользовательского интерфейса \_ PKEY \_ KeyTip не ограничена.</span><span class="sxs-lookup"><span data-stu-id="fa83d-111">The maximum length of UI\_PKEY\_Keytip is unbounded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa83d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="fa83d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa83d-113">Свойства ресурса</span><span class="sxs-lookup"><span data-stu-id="fa83d-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="fa83d-114">**Command. keytip**</span><span class="sxs-lookup"><span data-stu-id="fa83d-114">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




