---
title: UI_PKEY_Label
description: Определяет \_ свойство метки PKEY пользовательского интерфейса \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888652"
---
# <a name="ui_pkey_label"></a><span data-ttu-id="18ab3-103">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="18ab3-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="18ab3-104">Определяет \_ свойство метки PKEY пользовательского интерфейса \_ .</span><span class="sxs-lookup"><span data-stu-id="18ab3-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="18ab3-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18ab3-105">Remarks</span></span>

<span data-ttu-id="18ab3-106">\_Метка PKEY пользовательского интерфейса \_ используется приложением для запроса текста метки вкладок, групп, кнопок, элементов коллекции и других элементов управления ленты.</span><span class="sxs-lookup"><span data-stu-id="18ab3-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="18ab3-107">Windows 8 и более новые: изображение кнопки [меню приложения](windowsribbon-controls-applicationmenu.md) изменилось на метка: **файл**.</span><span class="sxs-lookup"><span data-stu-id="18ab3-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="18ab3-108">Не рекомендуется использовать файл в качестве метки для любой из вкладок.</span><span class="sxs-lookup"><span data-stu-id="18ab3-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="18ab3-109">Значение свойства — это строка, ограниченная любой последовательностью символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="18ab3-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="18ab3-110">Используйте ссылку на символ XML универсальной кодировки (UCS) `&#xA;` для указания разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="18ab3-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="18ab3-111">Выравнивание по правому краю не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="18ab3-111">Right alignment is not supported.</span></span>

<span data-ttu-id="18ab3-112">Максимальная длина \_ метки PKEY пользовательского интерфейса \_ не ограничена.</span><span class="sxs-lookup"><span data-stu-id="18ab3-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="18ab3-113">Если команда предоставляется через пункт меню, а значение [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или \_ подпись PKEY пользовательского интерфейса \_ содержит букву, предшествующую амперсанду, как показано в следующем примере, эта буква рассматривается как KeyTip и сочетание клавиш для этой команды в инфраструктуре Ribbon.</span><span class="sxs-lookup"><span data-stu-id="18ab3-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="18ab3-114">Чтобы отобразить знак амперсанда в метке, необходимо экранировать Специальный символ с двойным амперсандом ( `&&` ), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="18ab3-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="18ab3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="18ab3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ab3-116">Свойства ресурса</span><span class="sxs-lookup"><span data-stu-id="18ab3-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="18ab3-117">**Command. Лабелтитле**</span><span class="sxs-lookup"><span data-stu-id="18ab3-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="18ab3-118">UI \_ PKEY \_ лабелдескриптион</span><span class="sxs-lookup"><span data-stu-id="18ab3-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




